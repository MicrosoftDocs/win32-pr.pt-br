---
title: Exemplo de código de renderização
description: Exemplo de código de renderização
ms.assetid: 14978cf4-47fa-4b2e-ba51-799be873dc8a
keywords:
- visualizações, código de exemplo
- visualizações personalizadas, código de exemplo
- visualizações, função render
- visualizações personalizadas, função render
- Função render, código de exemplo
- exemplos, processar função para visualizações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a1ee5d00bc1aed5bd8bd91880e43e2ac2d1f6bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005760"
---
# <a name="sample-render-code"></a><span data-ttu-id="d32e2-109">Exemplo de código de renderização</span><span class="sxs-lookup"><span data-stu-id="d32e2-109">Sample Render Code</span></span>

<span data-ttu-id="d32e2-110">Aqui está um código de exemplo que usa a função **render** para desenhar uma linha na tela.</span><span class="sxs-lookup"><span data-stu-id="d32e2-110">Here is some sample code that uses the **Render** function to draw a line across the screen.</span></span> <span data-ttu-id="d32e2-111">A altura da linha é definida pelo valor de formato de onda.</span><span class="sxs-lookup"><span data-stu-id="d32e2-111">The height of the line is defined by the waveform value.</span></span>


```C++
STDMETHODIMP CStock::Render(TimedLevel *pLevels, HDC hdc, RECT *prc)
{
    // Create new brushes and pens.
    HBRUSH hNewBrush = ::CreateSolidBrush( 0 );
    // Create a new solid pen the color of the foreground.
    HPEN hNewPen = ::CreatePen( PS_SOLID, 0, m_clrForeground );


    // Add the pen to the device context.
    HPEN hOldPen= static_cast<HPEN>(::SelectObject( hdc, hNewPen ));

    // Fill the background with the black brush.
    ::FillRect( hdc, prc, hNewBrush );

    // Get the y value from the waveform.
    int y = pLevels->waveform[0][0];

    // Draw the line from left to right.
    ::MoveToEx( hdc, prc->left, y, NULL);  
    ::LineTo(hdc, prc->right, y); 

    // Delete your brush.
    if (hNewBrush)
    {
        ::DeleteObject( hNewBrush );
    }
    // Delete your pen.
    if (hNewPen)
    {
        ::SelectObject( hdc, hOldPen );
        ::DeleteObject( hNewPen );
    }

    // You're done for this round.
    return S_OK;
}

```



<span data-ttu-id="d32e2-112">A função **render** é onde ocorre o trabalho principal do seu código.</span><span class="sxs-lookup"><span data-stu-id="d32e2-112">The **Render** function is where the main work of your code takes place.</span></span> <span data-ttu-id="d32e2-113">Sempre que o Windows Media Player usar um instantâneo do áudio, ele chamará essa função e seu código será executado.</span><span class="sxs-lookup"><span data-stu-id="d32e2-113">Every time Windows Media Player takes a snapshot of the audio, it will call this function and your code will run.</span></span>

<span data-ttu-id="d32e2-114">Esse código executa as seguintes tarefas.</span><span class="sxs-lookup"><span data-stu-id="d32e2-114">This code performs the following tasks.</span></span> <span data-ttu-id="d32e2-115">Consulte o SDK da plataforma Microsoft Windows para Windows de 32 bits para obter mais detalhes sobre funções específicas.</span><span class="sxs-lookup"><span data-stu-id="d32e2-115">Refer to the Microsoft Windows Platform SDK for 32-bit Windows for more details about specific functions.</span></span>

## <a name="creating-objects"></a><span data-ttu-id="d32e2-116">Criando objetos</span><span class="sxs-lookup"><span data-stu-id="d32e2-116">Creating Objects</span></span>

<span data-ttu-id="d32e2-117">Normalmente, você usará as funções de desenho que vêm com a interface gráfica de vídeo (GDI) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d32e2-117">Usually you will be using the drawing functions that come with the Microsoft Windows Graphical Display Interface (GDI).</span></span> <span data-ttu-id="d32e2-118">Você precisa criar canetas para desenhar linhas e pincéis para preencher áreas.</span><span class="sxs-lookup"><span data-stu-id="d32e2-118">You need to create pens to draw lines and brushes to fill areas.</span></span>

<span data-ttu-id="d32e2-119">Um pincel preto sólido é criado para preencher o plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="d32e2-119">A solid black brush is created to fill in the background.</span></span>

<span data-ttu-id="d32e2-120">Uma caneta sólida é criada para desenhar uma linha.</span><span class="sxs-lookup"><span data-stu-id="d32e2-120">A solid pen is created to draw a line.</span></span> <span data-ttu-id="d32e2-121">A cor será a cor de primeiro plano, conforme definido pela capa que vai exibir a visualização.</span><span class="sxs-lookup"><span data-stu-id="d32e2-121">The color will be the foreground color as defined by the skin that is going to display the visualization.</span></span>

## <a name="adding-the-object-to-the-dc"></a><span data-ttu-id="d32e2-122">Adicionando o objeto ao controlador de domínio</span><span class="sxs-lookup"><span data-stu-id="d32e2-122">Adding the Object to the DC</span></span>

<span data-ttu-id="d32e2-123">Você precisa adicionar a caneta ao contexto do dispositivo (DC).</span><span class="sxs-lookup"><span data-stu-id="d32e2-123">You need to add the pen to the device context (DC).</span></span> <span data-ttu-id="d32e2-124">O DC é a parte da memória em que todos os dados e objetos de desenho são armazenados.</span><span class="sxs-lookup"><span data-stu-id="d32e2-124">The DC is the portion of memory that all drawing data and objects are stored in.</span></span> <span data-ttu-id="d32e2-125">Essencialmente, o DC é o Gerenciador de tráfego de janela que mantém o controle de tudo gráfico.</span><span class="sxs-lookup"><span data-stu-id="d32e2-125">Essentially the DC is the window traffic manager that keeps track of everything graphical.</span></span>

<span data-ttu-id="d32e2-126">Você precisa *converter* o objeto de caneta criado e armazená-lo como uma caneta antiga.</span><span class="sxs-lookup"><span data-stu-id="d32e2-126">You need to *cast* the pen object you created and store it as an old pen.</span></span> <span data-ttu-id="d32e2-127">Use esta técnica de codificação para todas as novas canetas.</span><span class="sxs-lookup"><span data-stu-id="d32e2-127">Use this coding technique for all new pens.</span></span> <span data-ttu-id="d32e2-128">Essa técnica é necessária para a programação de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d32e2-128">This technique is required for 32-bit programming.</span></span>

## <a name="filling-in-the-background"></a><span data-ttu-id="d32e2-129">Preenchendo o plano de fundo</span><span class="sxs-lookup"><span data-stu-id="d32e2-129">Filling in the Background</span></span>

<span data-ttu-id="d32e2-130">Agora você está pronto para desenhar.</span><span class="sxs-lookup"><span data-stu-id="d32e2-130">You now are ready to draw.</span></span> <span data-ttu-id="d32e2-131">A função **FillRect** preencherá o retângulo da janela, conforme definido pelos parâmetros da função **render** .</span><span class="sxs-lookup"><span data-stu-id="d32e2-131">The **FillRect** function will fill the rectangle of the window, as defined by the parameters of the **Render** function.</span></span> <span data-ttu-id="d32e2-132">O retângulo é preenchido com um pincel preto.</span><span class="sxs-lookup"><span data-stu-id="d32e2-132">The rectangle is filled with a black brush.</span></span>

## <a name="getting-audio-data"></a><span data-ttu-id="d32e2-133">Obtendo dados de áudio</span><span class="sxs-lookup"><span data-stu-id="d32e2-133">Getting Audio Data</span></span>

<span data-ttu-id="d32e2-134">Em seguida, o código obtém alguns dados de áudio do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d32e2-134">Next the code gets some audio data from Windows Media Player.</span></span> <span data-ttu-id="d32e2-135">Usando a matriz de formato de onda, você pode obter o valor atual da energia de áudio no momento em que o instantâneo foi tirado.</span><span class="sxs-lookup"><span data-stu-id="d32e2-135">By using the waveform array, you can get the current value of the audio power at the moment the snapshot was taken.</span></span> <span data-ttu-id="d32e2-136">Nesse caso, você está pegando os dados de áudio do canal esquerdo.</span><span class="sxs-lookup"><span data-stu-id="d32e2-136">In this case, you are taking the audio data of the left channel.</span></span> <span data-ttu-id="d32e2-137">O primeiro valor na matriz é o primeiro 1024th do instantâneo de energia de áudio.</span><span class="sxs-lookup"><span data-stu-id="d32e2-137">The first value in the array is the first 1024th of the audio power snapshot.</span></span>

<span data-ttu-id="d32e2-138">Essas informações serão usadas para exibir uma linha cuja altura corresponderá ao instantâneo de energia de áudio.</span><span class="sxs-lookup"><span data-stu-id="d32e2-138">This information will be used to display a line whose height will match the audio power snapshot.</span></span>

## <a name="draw-the-line"></a><span data-ttu-id="d32e2-139">Desenhar a linha</span><span class="sxs-lookup"><span data-stu-id="d32e2-139">Draw the Line</span></span>

<span data-ttu-id="d32e2-140">A linha é desenhada da esquerda para a direita usando as funções **MoveToEx** e **LineTo** GDI.</span><span class="sxs-lookup"><span data-stu-id="d32e2-140">The line is drawn from left to right using the **MoveToEx** and **LineTo** GDI functions.</span></span>

<span data-ttu-id="d32e2-141">Primeiro, mova a caneta para o ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="d32e2-141">First you move the pen to the starting point.</span></span> <span data-ttu-id="d32e2-142">Nesse caso, x e y são usados para definir os valores da esquerda para a direita e de cima para baixo que o usuário verá na tela.</span><span class="sxs-lookup"><span data-stu-id="d32e2-142">In this case, x and y are used to define the left-to-right and top-to-bottom values the user will see on the screen.</span></span> <span data-ttu-id="d32e2-143">X é definido pelo retângulo PRC e especificamente pelo valor de PRC->esquerda.</span><span class="sxs-lookup"><span data-stu-id="d32e2-143">X is defined by the rectangle prc and specifically by the value of prc->left.</span></span> <span data-ttu-id="d32e2-144">Y é definido como o valor dos dados da forma de onda nesse momento.</span><span class="sxs-lookup"><span data-stu-id="d32e2-144">Y is defined as the value of the waveform data at that moment.</span></span>

<span data-ttu-id="d32e2-145">Em seguida, você desenha uma linha para o outro lado da janela.</span><span class="sxs-lookup"><span data-stu-id="d32e2-145">Then you draw a line to the other side of the window.</span></span> <span data-ttu-id="d32e2-146">O ponto para o qual você desenha a linha é novamente um valor x, y.</span><span class="sxs-lookup"><span data-stu-id="d32e2-146">The point you draw the line to is again an x, y value.</span></span> <span data-ttu-id="d32e2-147">X é definido pelo retângulo PRC, mas desta vez por prc->direito.</span><span class="sxs-lookup"><span data-stu-id="d32e2-147">X is defined by the rectangle prc, but this time by prc->right.</span></span> <span data-ttu-id="d32e2-148">Y ainda é definido pelos dados de forma de onda e é o mesmo que o ponto de início, pois você está desenhando uma linha reta da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="d32e2-148">Y is still defined by the waveform data and is the same as the point you started from, because you are drawing a straight line from left to right.</span></span>

## <a name="clean-up-everything"></a><span data-ttu-id="d32e2-149">Limpar tudo</span><span class="sxs-lookup"><span data-stu-id="d32e2-149">Clean up Everything</span></span>

<span data-ttu-id="d32e2-150">Você deve excluir os objetos que criar.</span><span class="sxs-lookup"><span data-stu-id="d32e2-150">You must delete the objects you create.</span></span> <span data-ttu-id="d32e2-151">Especificamente, você deve excluir todos os pincéis e canetas que criar.</span><span class="sxs-lookup"><span data-stu-id="d32e2-151">Specifically you must delete any and all brushes and pens you create.</span></span> <span data-ttu-id="d32e2-152">É uma boa prática excluir canetas e pincéis quando você terminar de usá-las.</span><span class="sxs-lookup"><span data-stu-id="d32e2-152">It is good practice to delete pens and brushes when you finish using them.</span></span>

<span data-ttu-id="d32e2-153">Se você não excluí-las antes de concluir a implementação da função **render** , sua visualização falhará em um minuto ou menos.</span><span class="sxs-lookup"><span data-stu-id="d32e2-153">If you do not delete them before finishing your implementation of the **Render** function, your visualization will crash in a minute or less.</span></span> <span data-ttu-id="d32e2-154">Você deve manter uma contagem de canetas e pincéis e destruir cada uma delas.</span><span class="sxs-lookup"><span data-stu-id="d32e2-154">You must keep a count of your pens and brushes and destroy every single one.</span></span> <span data-ttu-id="d32e2-155">Tenha cuidado especialmente para não criar canetas dentro de um loop de código.</span><span class="sxs-lookup"><span data-stu-id="d32e2-155">Be especially careful not to create pens inside a code loop.</span></span>

<span data-ttu-id="d32e2-156">Use a técnica de codificação fornecida no exemplo para destruir suas canetas e pincéis.</span><span class="sxs-lookup"><span data-stu-id="d32e2-156">Use the coding technique given in the example to destroy your pens and brushes.</span></span>

-   <span data-ttu-id="d32e2-157">**Importante** Destrua suas canetas e pincéis!</span><span class="sxs-lookup"><span data-stu-id="d32e2-157">**Important** Destroy your pens and brushes!</span></span>

<span data-ttu-id="d32e2-158">Quando terminar de limpar, não se esqueça de retornar S \_ OK para que o Windows Media Player saiba que você concluiu o desenho.</span><span class="sxs-lookup"><span data-stu-id="d32e2-158">When you have finished cleaning up, be sure to return S\_OK so that Windows Media Player knows you are finished drawing.</span></span> <span data-ttu-id="d32e2-159">Depois de concluir, o desenho será transferido para a janela, outro instantâneo será criado, o **processamento** solicitará que seu código desenhe novamente e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="d32e2-159">Once you finish, your drawing will be transferred to the window, another snapshot will be taken, **Render** will ask your code to draw again, and so on.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d32e2-160">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d32e2-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d32e2-161">**Implementando renderização**</span><span class="sxs-lookup"><span data-stu-id="d32e2-161">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




