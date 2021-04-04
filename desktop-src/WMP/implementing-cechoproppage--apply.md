---
title: Implementando CEchoPropPage Apply
description: Implementando CEchoPropPage Apply
ms.assetid: e887b851-e623-4ec4-8d8b-165e4b21e116
keywords:
- Plug-ins do Windows Media Player, páginas de propriedades de exemplo de eco
- plug-ins, páginas de propriedades de exemplo de eco
- plug-ins de processamento de sinal digital, páginas de propriedades de exemplo de eco
- Plug-ins do DSP, páginas de propriedades de exemplo de eco
- Exemplo de plug-in do eco DSP, páginas de propriedades
- Exemplo de plug-in do eco DSP, método CEchoPropPage Apply
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bdca8a771d3e3e26923567f25bf7d19e968595e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822717"
---
# <a name="implementing-cechoproppageapply"></a><span data-ttu-id="f6e7a-109">Implementando CEchoPropPage:: apply</span><span class="sxs-lookup"><span data-stu-id="f6e7a-109">Implementing CEchoPropPage::Apply</span></span>

<span data-ttu-id="f6e7a-110">O método CEchoPropPage:: apply é implementado em EchoPropPage. cpp.</span><span class="sxs-lookup"><span data-stu-id="f6e7a-110">The CEchoPropPage::Apply method is implemented in EchoPropPage.cpp.</span></span> <span data-ttu-id="f6e7a-111">Ele é executado quando o usuário clica em **aplicar** na caixa de diálogo página de propriedades no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f6e7a-111">It executes when the user clicks **Apply** in the property page dialog box in Windows Media Player.</span></span> <span data-ttu-id="f6e7a-112">O código de exemplo do assistente de plug-in fornece uma implementação para lidar com uma única propriedade.</span><span class="sxs-lookup"><span data-stu-id="f6e7a-112">The plug-in wizard sample code provides an implementation to handle a single property.</span></span> <span data-ttu-id="f6e7a-113">Você pode modificar esse código para uma das propriedades de exemplo de eco e, em seguida, adicionar o código para armazenar o outro valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="f6e7a-113">You can modify this code for one of the Echo sample properties, and then add code to store the other property value.</span></span>

## <a name="declaring-the-apply-method-variables"></a><span data-ttu-id="f6e7a-114">Declarando as variáveis do método Apply</span><span class="sxs-lookup"><span data-stu-id="f6e7a-114">Declaring the Apply Method Variables</span></span>

<span data-ttu-id="f6e7a-115">Primeiro, você deve remover a declaração de fScaleFactor.</span><span class="sxs-lookup"><span data-stu-id="f6e7a-115">First, you must remove the declaration of fScaleFactor.</span></span> <span data-ttu-id="f6e7a-116">Em seguida, adicione declarações de variáveis que serão necessárias.</span><span class="sxs-lookup"><span data-stu-id="f6e7a-116">Then, add variable declarations that you will need.</span></span> <span data-ttu-id="f6e7a-117">O exemplo a seguir mostra as declarações de variável concluídas:</span><span class="sxs-lookup"><span data-stu-id="f6e7a-117">The following example shows the completed variable declarations:</span></span>


```
TCHAR   szStr[MAXSTRING] = { 0 };
DWORD   dwDelayTime = 1000;  // Initialize the delay time.
DWORD   dwWetmix = 50;       // Initialize a DWORD for effect level.
double  fWetmix = 0.50;      // Initialize a double for effect level.
```



## <a name="retrieving-the-values-from-the-property-page"></a><span data-ttu-id="f6e7a-118">Recuperando os valores da página de propriedades</span><span class="sxs-lookup"><span data-stu-id="f6e7a-118">Retrieving the Values from the Property Page</span></span>

<span data-ttu-id="f6e7a-119">Você deve implementar o código para recuperar e validar a entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="f6e7a-119">You must implement code to retrieve and validate the user input.</span></span> <span data-ttu-id="f6e7a-120">O exemplo de código a seguir recupera o valor de tempo de atraso da \_ caixa de edição do DelayTime da IDC e, em seguida, verifica se o valor está dentro de um intervalo especificado:</span><span class="sxs-lookup"><span data-stu-id="f6e7a-120">The following code example retrieves the delay time value from the IDC\_DELAYTIME edit box, and then verifies that the value is within a specified range:</span></span>


```
// Get the delay time value from the dialog box.
GetDlgItemText(IDC_DELAYTIME, szStr, sizeof(szStr) / sizeof(szStr[0]));

dwDelayTime = atoi(szStr);

// Make sure delay time is valid.
if ((dwDelayTime < 10) || (dwDelayTime > 2000))
{
    if (::LoadString(_Module.GetResourceInstance(), IDS_DELAYRANGEERROR, szStr, sizeof(szStr) / sizeof(szStr[0])))
    {
        MessageBox(szStr);
    }

    return E_FAIL;
}
```



<span data-ttu-id="f6e7a-121">Se a entrada do usuário não estiver no intervalo especificado, o código exibirá uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="f6e7a-121">If the user input is not in the specified range, the code displays a message box.</span></span> <span data-ttu-id="f6e7a-122">Observe o uso do recurso de cadeia de caracteres que você criou anteriormente para a mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="f6e7a-122">Notice the use of the string resource you created earlier for the error message.</span></span>

<span data-ttu-id="f6e7a-123">O exemplo a seguir recupera o nível de efeito da \_ caixa de edição WETMIX do IDC e, em seguida, verifica se o valor está dentro de um intervalo especificado:</span><span class="sxs-lookup"><span data-stu-id="f6e7a-123">The following example retrieves the effect level from the IDC\_WETMIX edit box and then verifies that the value is within a specified range:</span></span>


```
// Get the effects level value from the dialog box.
GetDlgItemText(IDC_WETMIX, szStr, sizeof(szStr) / sizeof(szStr[0]));

dwWetmix = atoi(szStr);

// Make sure wet mix value is valid.
if ((dwWetmix < 0) || (dwWetmix > 100))
{
    if (::LoadString(_Module.GetResourceInstance(), IDS_MIXRANGEERROR, szStr, sizeof(szStr) / sizeof(szStr[0])))
    {
        MessageBox(szStr);
    }

    return E_FAIL;
}
```



## <a name="storing-the-property-values-in-the-registry"></a><span data-ttu-id="f6e7a-124">Armazenando os valores de propriedade no registro</span><span class="sxs-lookup"><span data-stu-id="f6e7a-124">Storing the Property Values in the Registry</span></span>

<span data-ttu-id="f6e7a-125">Em seguida, seu código deve manter os novos valores de propriedade no registro.</span><span class="sxs-lookup"><span data-stu-id="f6e7a-125">Next, your code must persist the new property values to the registry.</span></span> <span data-ttu-id="f6e7a-126">O código a seguir armazena os dois valores de propriedade:</span><span class="sxs-lookup"><span data-stu-id="f6e7a-126">The following code stores both property values:</span></span>


```
// update the registry
CRegKey key;
LONG    lResult;

// Write the delay time value to the registry.
lResult = key.Create(HKEY_CURRENT_USER, kszPrefsRegKey);
if (ERROR_SUCCESS == lResult)
{
    lResult = key.SetValue( dwDelayTime , kszPrefsDelayTime );
}

// Write the wet mix value to the registry.
lResult = key.Create(HKEY_CURRENT_USER, kszPrefsRegKey);
if (ERROR_SUCCESS == lResult)
{
    lResult = key.SetValue( dwWetmix , kszPrefsWetmix );
}
```



## <a name="updating-the-echo-plug-in-property-values"></a><span data-ttu-id="f6e7a-127">Atualizando os valores de propriedade de plug-in de eco</span><span class="sxs-lookup"><span data-stu-id="f6e7a-127">Updating the Echo Plug-in Property Values</span></span>

<span data-ttu-id="f6e7a-128">O método **Apply** deve informar ao plug-in de eco que os valores de propriedade foram alterados.</span><span class="sxs-lookup"><span data-stu-id="f6e7a-128">The **Apply** method must inform the Echo plug-in that the property values have changed.</span></span> <span data-ttu-id="f6e7a-129">O código a seguir chama o método Property Put de cada propriedade usando o ponteiro de interface recuperado em CEchoPropPage:: SetObjects:</span><span class="sxs-lookup"><span data-stu-id="f6e7a-129">The following code calls the property put method for each property using the interface pointer retrieved in CEchoPropPage::SetObjects:</span></span>


```
// update the plug-in
if (m_spEcho)
{
    m_spEcho->put_delay(dwDelayTime);

    // Convert the wet mix value from DWORD to double.
    fWetmix = (double)dwWetmix / 100;
    m_spEcho->put_wetmix(fWetmix);
}
```



<span data-ttu-id="f6e7a-130">Observe que o valor de combinação úmida é convertido em ponto flutuante antes de ser passado para o plug-in.</span><span class="sxs-lookup"><span data-stu-id="f6e7a-130">Notice that the wet mix value is converted to floating point before being passed to the plug-in.</span></span>

## <a name="disabling-the-apply-button"></a><span data-ttu-id="f6e7a-131">Desabilitando o botão aplicar</span><span class="sxs-lookup"><span data-stu-id="f6e7a-131">Disabling the Apply Button</span></span>

<span data-ttu-id="f6e7a-132">Como etapa final, seu código deve desabilitar a aplicação na caixa de diálogo página de propriedades como um sinal para o usuário que os valores foram atualizados com êxito.</span><span class="sxs-lookup"><span data-stu-id="f6e7a-132">As a final step, your code should disable Apply in the property page dialog box as a signal to the user that the values have been successfully updated.</span></span> <span data-ttu-id="f6e7a-133">Isso requer uma única linha de código a seguir:</span><span class="sxs-lookup"><span data-stu-id="f6e7a-133">This requires the following single line of code:</span></span>


```
m_bDirty = FALSE; // Tell the property page to disable Apply.
```



## <a name="related-topics"></a><span data-ttu-id="f6e7a-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f6e7a-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6e7a-135">**Modificando a página de propriedades de exemplo de eco**</span><span class="sxs-lookup"><span data-stu-id="f6e7a-135">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




