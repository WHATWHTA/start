using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class SPEED1 : MonoBehaviour
{
    public Rigidbody2D rb;
    public Animator anim;
    public float speed;
    public float jumpforce;
    
    
    // Start is called before the first frame update
    void Start()
    {

    }

    //Update is called once per frame  每秒处理的函数
    void FixedUpdate()
    {
        Movement();
    }

    void Movement()
    {
        //变量获得我们我们在键盘上输入的数值。
        float horizontalmove = Input.GetAxis("Horizontal");

        //GetAxisRaw方法获得3个数值 -1 ，0,1，所以按照逻辑，当 facedirection = -1的时候，就像小狐狸面向左边。
        float facedirection = Input.GetAxisRaw("Horizontal");

        //如果数值不等于 0 ，那么数值就是再被操作，进行if判断
        if (horizontalmove != 0)
        {
            //Vector2 方法控制角(jué)色位置
            rb.velocity = new Vector2(horizontalmove * speed * Time.deltaTime, rb.velocity.y);
            //调用动画的方法
            anim.SetFloat("running",Mathf.Abs(facedirection));
        }
        //我们可以在

        if (facedirection != 0)
        {
            //Vector3 方法控制角色轉向
            transform.localScale = new Vector3(facedirection,1,1);
        }
        //角色跳跃
        if(Input.GetButtonDown("Jump"))
        {
            rb.velocity = new Vector2(rb.velocity.x, jumpforce * Time.deltaTime);
            anim.SetBool("jumping",true);
            
        }
    }
 
}
