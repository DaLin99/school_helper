<template>
	<div class="recruit-info-container">
		<div
			class="recruit-info-item"
			v-for="(item, index) in recruitInfoList"
			:key="index"
		>
			<div class="container-left">
				<div class="flex-box hover-height-light">
					<span>{{ item.workType }}</span>
					<span>{{ item.salary }}</span>
				</div>
				<div class="flex-box">
					<span>{{ item.company }}</span>
					<span>{{ item.palce }}</span>
				</div>
				<div class="flex-box">
					<span
						v-for="(
							requirementItem, requirementIndex
						) in item.requirement"
						:key="requirementIndex"
					>
						{{ requirementItem }}
					</span>
					<span class="date">{{ item.date }}</span>
				</div>
			</div>
			<div class="container-right">
				<img class="company-img" :src="item.imgPath" alt="" />
			</div>
		</div>
	</div>
</template>

<script>
export default {
	data() {
		return {
			recruitInfoList: [
				{
					company: "快手科技信息有限公司",
					workType: "前端工程师-校招实习",
					salary: "200/天",
					palce: "北京",
					requirement: ["在校应届", "本科"],
					imgPath: "../../static/image/activity-bgc.png",
					date: "2021-1-2",
				},
				{
					company: "快手科技信息有限公司",
					workType: "前端工程师-校招实习",
					salary: "200/天",
					palce: "北京",
					requirement: ["在校应届", "本科"],
					imgPath: "../../static/image/activity-bgc.png",
					date: "2021-1-2",
				},
			],
		};
	},
	methods: {},
};
</script>

<style lang="less" scope>
@import "./recruitInfo.less";
</style>
