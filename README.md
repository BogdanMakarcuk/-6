const TRIANGLES: usize = 3; // Кількість трикутників у ялинці
fn main() {
    let mut height = 1;
    for i in 0..TRIANGLES {
    
    (0..=i * 2).for_each(|row| {
            let spaces = " ".repeat(TRIANGLES * 2 - row);
            let stars = "*".repeat(row * 2 + 1);
            println!("{}{}", spaces, stars);
        });
        height += 2;
    }
    
    // Малюємо стовбур
    let trunk_width = 3;
    let trunk_height = 2;
    let trunk_spaces = " ".repeat(TRIANGLES * 2 - 1);
    (0..trunk_height).for_each(|_| println!("{}{}", trunk_spaces, "|".repeat(trunk_width)));
}
