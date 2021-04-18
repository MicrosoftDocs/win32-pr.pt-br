---
title: Modificando a propriedade Scale
description: Modificando a propriedade Scale
ms.assetid: 32ebaa54-ed13-4b10-8876-bf8e188d7317
keywords:
- Plug-ins do Windows Media Player, propriedades de exemplo de eco
- plug-ins, propriedades de exemplo de eco
- plug-ins de processamento de sinal digital, propriedades de exemplo de eco
- Plug-ins do DSP, propriedades de exemplo de eco
- Exemplo de plug-in do DSP de eco, Propriedade Scale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd91e2315db9d0d1e14d2aec55f79a8b05c442ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105763909"
---
# <a name="modifying-the-scale-property"></a><span data-ttu-id="64387-108">Modificando a propriedade Scale</span><span class="sxs-lookup"><span data-stu-id="64387-108">Modifying the Scale Property</span></span>

<span data-ttu-id="64387-109">A implementação do assistente padrão expõe a propriedade Scale.</span><span class="sxs-lookup"><span data-stu-id="64387-109">The default wizard implementation exposes the scale property.</span></span> <span data-ttu-id="64387-110">Você pode alterar a implementação existente para expor a propriedade tempo de atraso em vez disso.</span><span class="sxs-lookup"><span data-stu-id="64387-110">You can change the existing implementation to expose the delay time property instead.</span></span>

<span data-ttu-id="64387-111">Primeiro, use o exemplo a seguir para alterar os protótipos de função para obter \_ escala e colocar \_ escala em Echo. h.</span><span class="sxs-lookup"><span data-stu-id="64387-111">First, use the following example to change the function prototypes for get\_scale and put\_scale in Echo.h.</span></span> <span data-ttu-id="64387-112">Altere o nome dos métodos e os tipos de dados para os parâmetros:</span><span class="sxs-lookup"><span data-stu-id="64387-112">Change the name of the methods and the data types for the parameters:</span></span>


```C++
// IEcho methods
STDMETHOD(get_delay)(DWORD *pVal);
STDMETHOD(put_delay)(DWORD newVal);

```



<span data-ttu-id="64387-113">Em seguida, altere as implementações dos \_ métodos obter escala e colocar \_ escala em Echo. cpp.</span><span class="sxs-lookup"><span data-stu-id="64387-113">Next, change the implementations of the get\_scale and put\_scale methods in Echo.cpp.</span></span> <span data-ttu-id="64387-114">Faça com que o código corresponda aos seguintes exemplos:</span><span class="sxs-lookup"><span data-stu-id="64387-114">Make the code match the following examples:</span></span>


```C++
// Formerly get_scale
STDMETHODIMP CEcho::get_delay(DWORD *pVal)
{
    if ( NULL == pVal )
    {
        return E_POINTER;
    }

    *pVal = m_dwDelayTime;

    return S_OK;
}

// Formerly put_scale
STDMETHODIMP CEcho::put_delay(DWORD newVal)
{
    m_dwDelayTime = newVal;

    return S_OK;
}

```



<span data-ttu-id="64387-115">O código de exemplo anterior altera os nomes de método e os tipos de dados de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="64387-115">The preceding example code changes the method names and the parameter data types.</span></span> <span data-ttu-id="64387-116">O nome da variável de membro deve ter sido alterado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="64387-116">The member variable name should have been changed previously.</span></span> <span data-ttu-id="64387-117">Lembre-se de alterar os comentários que introduzem cada método também.</span><span class="sxs-lookup"><span data-stu-id="64387-117">Remember to change the comments that introduce each method as well.</span></span>

<span data-ttu-id="64387-118">Agora, altere a definição da interface.</span><span class="sxs-lookup"><span data-stu-id="64387-118">Now, change the interface definition.</span></span> <span data-ttu-id="64387-119">O código a seguir substitui o código na declaração de interface IEcho em Echo. idl:</span><span class="sxs-lookup"><span data-stu-id="64387-119">The following code replaces the code in the IEcho interface declaration in Echo.idl:</span></span>


```C++
HRESULT get_delay([out] DWORD *pVal);
HRESULT put_delay([in] DWORD newVal);

```



## <a name="related-topics"></a><span data-ttu-id="64387-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="64387-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64387-121">**Propriedades de exemplo de eco**</span><span class="sxs-lookup"><span data-stu-id="64387-121">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 




