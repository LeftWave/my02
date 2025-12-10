# my02
2
def student_grade_system():
    # 存储学生信息：姓名-成绩字典
    students = {}
    while True:
        print("\n===== 学生成绩管理系统 =====")
        print("1. 添加学生成绩")
        print("2. 查询学生成绩")
        print("3. 修改学生成绩")
        print("4. 显示所有学生成绩")
        print("5. 退出系统")
        choice = input("请输入操作序号（1-5）：")
        
        if choice == "1":
            name = input("请输入学生姓名：")
            score = float(input("请输入学生成绩："))
            students[name] = score
            print(f"✅ 成功添加 {name} 的成绩：{score}")
        elif choice == "2":
            name = input("请输入要查询的学生姓名：")
            if name in students:
                print(f"📊 {name} 的成绩为：{students[name]}")
            else:
                print("❌ 未找到该学生信息！")
        elif choice == "3":
            name = input("请输入要修改的学生姓名：")
            if name in students:
                new_score = float(input("请输入新成绩："))
                students[name] = new_score
                print(f"✅ 成功修改 {name} 的成绩为：{new_score}")
            else:
                print("❌ 未找到该学生信息！")
        elif choice == "4":
            if not students:
                print("📃 暂无学生成绩数据！")
            else:
                print("\n📃 所有学生成绩如下：")
                for name, score in students.items():
                    print(f"姓名：{name}\t成绩：{score}")
        elif choice == "5":
            print("👋 感谢使用，系统退出！")
            break
        else:
            print("❌ 输入错误，请输入1-5的序号！")

# 启动系统
student_grade_system()
