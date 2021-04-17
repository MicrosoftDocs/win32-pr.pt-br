---
title: Implementando CEchoPropPage OnInitDialog
description: Implementando CEchoPropPage OnInitDialog
ms.assetid: 568989b0-bc07-480f-8b5c-41bbada713f8
keywords:
- Plug-ins do Windows Media Player, páginas de propriedades de exemplo de eco
- plug-ins, páginas de propriedades de exemplo de eco
- plug-ins de processamento de sinal digital, páginas de propriedades de exemplo de eco
- Plug-ins do DSP, páginas de propriedades de exemplo de eco
- Exemplo de plug-in do eco DSP, páginas de propriedades
- Exemplo de plug-in do eco DSP, método CEchoPropPage OnInitDialog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0874c750914b5caecf86ffa61a0c42d38bb1c02e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105813153"
---
# <a name="implementing-cechoproppageoninitdialog"></a><span data-ttu-id="bc76c-109">Implementando CEchoPropPage:: OnInitDialog</span><span class="sxs-lookup"><span data-stu-id="bc76c-109">Implementing CEchoPropPage::OnInitDialog</span></span>

<span data-ttu-id="bc76c-110">O método **CEchoPropPage:: OnInitDialog** é implementado em EchoPropPage. cpp.</span><span class="sxs-lookup"><span data-stu-id="bc76c-110">The **CEchoPropPage::OnInitDialog** method is implemented in EchoPropPage.cpp.</span></span> <span data-ttu-id="bc76c-111">Ele é executado quando a caixa de diálogo página de propriedades é chamada.</span><span class="sxs-lookup"><span data-stu-id="bc76c-111">It executes when the property page dialog box is invoked.</span></span> <span data-ttu-id="bc76c-112">O código nesse método precisa recuperar os valores de propriedade atuais e exibi-los na caixa de edição correta.</span><span class="sxs-lookup"><span data-stu-id="bc76c-112">The code in this method needs to retrieve the current property values and display them in the correct edit box.</span></span> <span data-ttu-id="bc76c-113">O código de exemplo do assistente de plug-in fornece uma implementação para uma única propriedade.</span><span class="sxs-lookup"><span data-stu-id="bc76c-113">The plug-in wizard sample code provides an implementation for a single property.</span></span> <span data-ttu-id="bc76c-114">Você pode modificar esse código para uma das propriedades de exemplo de eco e, em seguida, adicionar o código para recuperar o segundo valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="bc76c-114">You can modify this code for one of the Echo sample properties, and then add code to retrieve the second property value.</span></span>

## <a name="declaring-the-oninitdialog-method-variables"></a><span data-ttu-id="bc76c-115">Declarando as variáveis do método OnInitDialog</span><span class="sxs-lookup"><span data-stu-id="bc76c-115">Declaring the OnInitDialog Method Variables</span></span>

<span data-ttu-id="bc76c-116">Primeiro, você deve remover a declaração de fScaleFactor e substituí-la pelas seguintes declarações de variável:</span><span class="sxs-lookup"><span data-stu-id="bc76c-116">First, you must remove the declaration of fScaleFactor and replace it with the following variable declarations:</span></span>


```
DWORD  dwDelayTime = 1000;    // Default delay time.
DWORD  dwWetmix = 50;         // Default wet mix DWORD.
double fWetmix =  0.50;       // Default wet mix double.
```



## <a name="retrieving-the-current-values-from-the-plug-in"></a><span data-ttu-id="bc76c-117">Recuperando os valores atuais do plug-in</span><span class="sxs-lookup"><span data-stu-id="bc76c-117">Retrieving the Current Values from the Plug-in</span></span>

<span data-ttu-id="bc76c-118">O código deve tentar recuperar os valores de propriedade atuais do plug-in de eco.</span><span class="sxs-lookup"><span data-stu-id="bc76c-118">The code should next attempt to retrieve the current property values from the Echo plug-in.</span></span> <span data-ttu-id="bc76c-119">O exemplo a seguir tenta recuperar cada propriedade:</span><span class="sxs-lookup"><span data-stu-id="bc76c-119">The following example attempts to retrieve each property:</span></span>


```
if (m_spEcho)
{
    m_spEcho->get_delay(&dwDelayTime);
    m_spEcho->get_wetmix(&fWetmix);
    // Convert wet mix from double to DWORD.
    dwWetmix = (DWORD)(fWetmix * 100);
}
```



<span data-ttu-id="bc76c-120">A caixa de diálogo exibe o valor de nível de efeitos para o usuário como um inteiro, mas o plug-in armazena o valor como um número de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="bc76c-120">The dialog box displays the effects level value to the user as an integer, but the plug-in stores the value as a floating-point number.</span></span> <span data-ttu-id="bc76c-121">Portanto, o código converte o valor de ponto flutuante em um valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="bc76c-121">Therefore, the code converts the floating-point value to a **DWORD** value.</span></span>

## <a name="retrieving-the-current-values-from-the-registry"></a><span data-ttu-id="bc76c-122">Recuperando os valores atuais do registro</span><span class="sxs-lookup"><span data-stu-id="bc76c-122">Retrieving the Current Values from the Registry</span></span>

<span data-ttu-id="bc76c-123">Se a página de propriedades não puder recuperar os valores atuais do plug-in, ele deverá tentar lê-los no registro.</span><span class="sxs-lookup"><span data-stu-id="bc76c-123">If the property page cannot retrieve the current values from the plug-in, it must attempt to read them from the registry.</span></span> <span data-ttu-id="bc76c-124">O código a seguir lê cada valor de propriedade:</span><span class="sxs-lookup"><span data-stu-id="bc76c-124">The following code reads each property value:</span></span>


```
else // Otherwise, read values from registry
{
    CRegKey key;
    LONG    lResult;

    lResult = key.Open(HKEY_CURRENT_USER, kszPrefsRegKey, KEY_READ);
    if (ERROR_SUCCESS == lResult)
    {
        DWORD   dwValue = 0;

        // Read the delay time.
        lResult = key.QueryValue(dwValue, kszPrefsDelayTime );
        if (ERROR_SUCCESS == lResult)
        {
            dwDelayTime = dwValue;
        }

        // Read the wet mix value.
        lResult = key.QueryValue(dwValue, kszPrefsWetmix );
        if (ERROR_SUCCESS == lResult)
        {
            dwWetmix = dwValue;
        }
    }
}
```



<span data-ttu-id="bc76c-125">Observe o uso das constantes do registro que você criou anteriormente.</span><span class="sxs-lookup"><span data-stu-id="bc76c-125">Notice the use of the registry constants you created previously.</span></span>

## <a name="displaying-the-values-to-the-user"></a><span data-ttu-id="bc76c-126">Exibindo os valores para o usuário</span><span class="sxs-lookup"><span data-stu-id="bc76c-126">Displaying the Values to the User</span></span>

<span data-ttu-id="bc76c-127">Por fim, a página de propriedades deve exibir os valores nos controles corretos da caixa de edição.</span><span class="sxs-lookup"><span data-stu-id="bc76c-127">Finally, the property page must display the values in the correct edit box controls.</span></span> <span data-ttu-id="bc76c-128">O código de exemplo a seguir demonstra isso:</span><span class="sxs-lookup"><span data-stu-id="bc76c-128">The following example code demonstrates this:</span></span>


```
 TCHAR   szStr[MAXSTRING];

// Display the delay time.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwDelayTime);
SetDlgItemText(IDC_DELAYTIME, szStr);

// Display the effect level.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwWetmix);
SetDlgItemText(IDC_WETMIX, szStr);
```



## <a name="related-topics"></a><span data-ttu-id="bc76c-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bc76c-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc76c-130">**Modificando a página de propriedades de exemplo de eco**</span><span class="sxs-lookup"><span data-stu-id="bc76c-130">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




