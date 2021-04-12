---
title: Lidando com eventos de aquisição de licença
description: Lidando com eventos de aquisição de licença
ms.assetid: e118bf09-1fa6-41b6-a6bb-3e8cb6097994
keywords:
- SDK do Windows Media Format, lidando com eventos de aquisição de licença
- SDK do Windows Media Format, eventos de aquisição de licença
- ASF (Advanced Systems Format), tratando eventos de aquisição de licença
- ASF (formato de sistemas avançados), tratando eventos de aquisição de licença
- ASF (Advanced Systems Format), eventos de aquisição de licença
- ASF (formato de sistemas avançados), eventos de aquisição de licença
- DRM (gerenciamento de direitos digitais), lidando com eventos de aquisição de licença
- DRM (gerenciamento de direitos digitais), manipulação de eventos de aquisição de licença
- DRM (gerenciamento de direitos digitais), eventos de aquisição de licença
- DRM (gerenciamento de direitos digitais), eventos de aquisição de licença
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e31fd5b108f41d5b0925918fdf1c83764bcf7e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365577"
---
# <a name="handling-license-acquisition-events"></a><span data-ttu-id="d21a9-113">Lidando com eventos de aquisição de licença</span><span class="sxs-lookup"><span data-stu-id="d21a9-113">Handling License Acquisition Events</span></span>

<span data-ttu-id="d21a9-114">Um aplicativo de leitor habilitado para DRM, em seu método de retorno de chamada [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) , lida com os quatro eventos a seguir relacionados ao processo de aquisição de licença:</span><span class="sxs-lookup"><span data-stu-id="d21a9-114">A DRM-enabled reader application, in its [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method, handles the following four events related to the license acquisition process:</span></span>

-   <span data-ttu-id="d21a9-115">**\_estado de \_ assinatura WMT LICENSEURL \_**</span><span class="sxs-lookup"><span data-stu-id="d21a9-115">**WMT\_LICENSEURL\_SIGNATURE\_STATE**</span></span>
-   <span data-ttu-id="d21a9-116">**WMT \_ sem \_ direitos**</span><span class="sxs-lookup"><span data-stu-id="d21a9-116">**WMT\_NO\_RIGHTS**</span></span>
-   <span data-ttu-id="d21a9-117">**WMT \_ sem \_ direitos \_ ex**</span><span class="sxs-lookup"><span data-stu-id="d21a9-117">**WMT\_NO\_RIGHTS\_EX**</span></span>
-   <span data-ttu-id="d21a9-118">**\_licença de aquisição do WMT \_**</span><span class="sxs-lookup"><span data-stu-id="d21a9-118">**WMT\_ACQUIRE\_LICENSE**</span></span>

<span data-ttu-id="d21a9-119">**\_estado de \_ assinatura WMT LICENSEURL \_**</span><span class="sxs-lookup"><span data-stu-id="d21a9-119">**WMT\_LICENSEURL\_SIGNATURE\_STATE**</span></span>

<span data-ttu-id="d21a9-120">Quando o componente DRM detecta conteúdo protegido pelo DRM versão 7, ele primeiro procura uma licença válida no sistema local.</span><span class="sxs-lookup"><span data-stu-id="d21a9-120">When the DRM component detects content protected by DRM version 7, it first looks for a valid license on the local system.</span></span> <span data-ttu-id="d21a9-121">Se não houver nenhum, ele avaliará a URL de aquisição de licença no cabeçalho DRM do arquivo e enviará um evento de **estado de \_ \_ assinatura \_ WMT LICENSEURL** *com uma* definição de valor para um dos valores de [**\_ \_ confiança WMT DRMLA**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust) , indicando se a URL é confiável, não confiável ou se foi violada.</span><span class="sxs-lookup"><span data-stu-id="d21a9-121">If none exists, it then evaluates the license acquisition URL in the file's DRM header and sends a **WMT\_LICENSEURL\_SIGNATURE\_STATE** event with *pValue* set to one of the [**WMT\_DRMLA\_TRUST**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust) values, indicating whether the URL is trusted, untrusted, or has been tampered with.</span></span> <span data-ttu-id="d21a9-122">Se a URL não for confiável, o aplicativo deverá avisar o usuário.</span><span class="sxs-lookup"><span data-stu-id="d21a9-122">If the URL is not trusted, then the application should warn the user.</span></span> <span data-ttu-id="d21a9-123">Se a URL tiver sido violada, o arquivo deverá ser considerado corrompido e o aplicativo não deverá navegar até a URL sem emitir um aviso forte ao usuário.</span><span class="sxs-lookup"><span data-stu-id="d21a9-123">If the URL has been tampered with, then the file should be considered corrupted, and the application should not navigate to the URL without issuing a strong warning the user.</span></span>

<span data-ttu-id="d21a9-124">**WMT \_ sem \_ direitos**</span><span class="sxs-lookup"><span data-stu-id="d21a9-124">**WMT\_NO\_RIGHTS**</span></span>

<span data-ttu-id="d21a9-125">O evento **WMT \_ nenhum \_ Rights** é enviado somente para conteúdo DRM versão 1, o que significa que a licença deve ser adquirida não silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="d21a9-125">The **WMT\_NO\_RIGHTS** event is sent only for DRM version 1 content, which means that the license must be acquired non-silently.</span></span> <span data-ttu-id="d21a9-126">Em outras palavras, o usuário deve navegar para uma página da Web para adquirir uma licença.</span><span class="sxs-lookup"><span data-stu-id="d21a9-126">In other words, the user must navigate to a Web page to acquire a license.</span></span> <span data-ttu-id="d21a9-127">A URL da página é recuperada como uma cadeia de caracteres terminada em nulo de caractere largo *do parâmetro de número de espaço* no método **OnStatus** .</span><span class="sxs-lookup"><span data-stu-id="d21a9-127">The URL for the page is retrieved as a wide-character null-terminated string from the *pValue* parameter in the **OnStatus** method.</span></span>

<span data-ttu-id="d21a9-128">Se apropriado, um aplicativo pode facilitar para o usuário navegar até a página da Web, seja abrindo o Internet Explorer em um processo separado ou hospedando o controle do navegador da Web.</span><span class="sxs-lookup"><span data-stu-id="d21a9-128">If appropriate, an application can make it easier for the user to navigate to the Web page, either by opening up Internet Explorer in a separate process or else by hosting the Web Browser control.</span></span> <span data-ttu-id="d21a9-129">No entanto, isso não é necessário.</span><span class="sxs-lookup"><span data-stu-id="d21a9-129">This is not required, however.</span></span> <span data-ttu-id="d21a9-130">Na pior das hipóteses, um aplicativo pode simplesmente exibir a URL para o usuário em uma caixa de mensagem e pedir para colá-la na barra de endereços do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="d21a9-130">At the very least, an application could simply display the URL to the user in a message box and prompt them to paste it into the address bar of Internet Explorer.</span></span> <span data-ttu-id="d21a9-131">O exemplo AudioPlayer demonstra o tratamento adequado do evento **WMT \_ no \_ Rights** , incluindo como formatar a cadeia de caracteres da URL e como usar o método **CreateProcess** para abrir o Internet Explorer e navegar até a URL especificada.</span><span class="sxs-lookup"><span data-stu-id="d21a9-131">The Audioplayer sample demonstrates proper handling of the **WMT\_NO\_RIGHTS** event, including how to format the URL string, and how to use the **CreateProcess** method to open Internet Explorer and navigate to the specified URL.</span></span>

<span data-ttu-id="d21a9-132">Como o aplicativo não tem como saber quando uma licença do DRM versão 1 foi adquirida, cabe ao usuário tentar abrir o arquivo novamente após adquirir a licença.</span><span class="sxs-lookup"><span data-stu-id="d21a9-132">Because the application has no way of knowing when a DRM version 1 license has been acquired, it is up to the user to attempt to open the file again after acquiring the license.</span></span>

<span data-ttu-id="d21a9-133">Esse mesmo processo de aquisição de licença não silenciosa também pode ser usado para licenças da versão 7, mas, nesse caso, o aplicativo pode primeiro chamar [**IWMDRMReader:: MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition).</span><span class="sxs-lookup"><span data-stu-id="d21a9-133">This same non-silent license acquisition process can also be used for version 7 licenses, but in this case the application can first call [**IWMDRMReader::MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition).</span></span> <span data-ttu-id="d21a9-134">Esse método fará com que o repositório de licenças local seja verificado repetidamente até que a licença do novo arquivo seja encontrada.</span><span class="sxs-lookup"><span data-stu-id="d21a9-134">This method will cause the local license store to be checked repeatedly until the license for the new file is found.</span></span> <span data-ttu-id="d21a9-135">Nesse ponto, o aplicativo receberá um evento **de \_ \_ licença de aquisição WMT** .</span><span class="sxs-lookup"><span data-stu-id="d21a9-135">At that point, the application will receive a **WMT\_ACQUIRE\_LICENSE** event.</span></span> <span data-ttu-id="d21a9-136">Para todas as licenças da versão 7, é recomendável que os aplicativos forneçam aos usuários a opção de obter licenças silenciosamente ou não silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="d21a9-136">For all version 7 licenses, it is recommended that applications give users the option to obtain licenses silently or non-silently.</span></span>

<span data-ttu-id="d21a9-137">**WMT \_ sem \_ direitos \_ ex**</span><span class="sxs-lookup"><span data-stu-id="d21a9-137">**WMT\_NO\_RIGHTS\_EX**</span></span>

<span data-ttu-id="d21a9-138">O evento **WMT \_ no \_ Rights \_ ex** indica que o conteúdo está protegido pelo DRM versão 7 e, portanto, o processo de aquisição de licença pode continuar silenciosamente ou não silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="d21a9-138">The **WMT\_NO\_RIGHTS\_EX** event indicates that the content is protected by DRM version 7, and therefore the license acquisition process can proceed either silently or non-silently.</span></span> <span data-ttu-id="d21a9-139">Em geral, a aquisição de licença silenciosa é mais conveniente para os usuários finais, embora algumas pessoas prefiram adquirir todas as licenças não silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="d21a9-139">In general, silent license acquisition is more convenient for end users, although some people prefer to acquire all licenses non-silently.</span></span> <span data-ttu-id="d21a9-140">Quando a aquisição de licença exige que o usuário envie pagamentos ou informações pessoais, o processo sempre deve ser executado de forma não silenciosa.</span><span class="sxs-lookup"><span data-stu-id="d21a9-140">When license acquisition requires the user to submit payment or personal information, the process should always be performed non-silently.</span></span> <span data-ttu-id="d21a9-141">A aquisição de licença não silenciosa é descrita acima no cabeçalho **WMT \_ nenhum \_ direito** .</span><span class="sxs-lookup"><span data-stu-id="d21a9-141">Non-silent license acquisition is described above under the **WMT\_NO\_RIGHTS** heading.</span></span> <span data-ttu-id="d21a9-142">A aquisição silenciosa continua da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d21a9-142">Silent acquisition proceeds as follows:</span></span>

1.  <span data-ttu-id="d21a9-143">Converta *o parâmetro de chegar a uma* estrutura de [**\_ \_ \_ dados obter licença do WM**](wm-get-license-data.md) e armazene a estrutura caso ela seja necessária posteriormente para aquisição de licença não silenciosa.</span><span class="sxs-lookup"><span data-stu-id="d21a9-143">Cast the *pValue* parameter to a [**WM\_GET\_LICENSE\_DATA**](wm-get-license-data.md) structure and store the structure in case it is needed later for non-silent license acquisition.</span></span>
2.  <span data-ttu-id="d21a9-144">Chame **QueryInterface** no objeto Reader para obter a interface [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) .</span><span class="sxs-lookup"><span data-stu-id="d21a9-144">Call **QueryInterface** on the reader object to obtain the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface.</span></span>
3.  <span data-ttu-id="d21a9-145">Chame [**IWMDRMReader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) e especifique 0x1 no parâmetro *dwFlags* para indicar a aquisição de linguagem silenciosa.</span><span class="sxs-lookup"><span data-stu-id="d21a9-145">Call [**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) and specify 0x1 in the *dwFlags* parameter to indicate silent language acquisition.</span></span> <span data-ttu-id="d21a9-146">Essa é uma chamada assíncrona que retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="d21a9-146">This is an asynchronous call that returns immediately.</span></span>
4.  <span data-ttu-id="d21a9-147">Aguarde o evento **de \_ \_ licença de aquisição WMT** .</span><span class="sxs-lookup"><span data-stu-id="d21a9-147">Wait for the **WMT\_ACQUIRE\_LICENSE** event.</span></span>

<span data-ttu-id="d21a9-148">**\_licença de aquisição do WMT \_**</span><span class="sxs-lookup"><span data-stu-id="d21a9-148">**WMT\_ACQUIRE\_LICENSE**</span></span>

<span data-ttu-id="d21a9-149">O evento de **\_ \_ licença de aquisição WMT** é enviado após a conclusão do processo de aquisição de licença para uma licença do DRM versão 7.</span><span class="sxs-lookup"><span data-stu-id="d21a9-149">The **WMT\_ACQUIRE\_LICENSE** event is sent after the license acquisition process is completed for a DRM version 7 license.</span></span> <span data-ttu-id="d21a9-150">[**IWMDRMReader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) faz com que esse evento seja enviado para aquisição silenciosa e [**MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition) faz com que ele seja enviado para aquisição não silenciosa.</span><span class="sxs-lookup"><span data-stu-id="d21a9-150">[**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) causes this event to be sent for silent acquisition, and [**MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition) causes it to be sent for non-silent acquisition.</span></span> <span data-ttu-id="d21a9-151">No manipulador de eventos, converta a um *ponteiro para uma* estrutura de [**\_ \_ \_ dados obter licença do WM**](wm-get-license-data.md) e examine o membro de **RH** para determinar se a licença foi adquirida com êxito.</span><span class="sxs-lookup"><span data-stu-id="d21a9-151">In your event handler, cast *pValue* to a pointer to a [**WM\_GET\_LICENSE\_DATA**](wm-get-license-data.md) structure and examine the **hr** member to determine whether the license was successfully acquired.</span></span> <span data-ttu-id="d21a9-152">Se **HR** for igual a NS \_ E \_ DRM \_ sem \_ direitos, isso indica que a licença deve ser adquirida não silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="d21a9-152">If **hr** equals NS\_E\_DRM\_NO\_RIGHTS, it indicates that the license must be acquired non-silently.</span></span> <span data-ttu-id="d21a9-153">Os aplicativos devem permitir que os usuários cancelem o processo de aquisição de licença a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="d21a9-153">Applications should enable users to cancel the license acquisition process at any time.</span></span> <span data-ttu-id="d21a9-154">Isso é feito chamando [**IWMDRMReader:: CancelLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancellicenseacquisition).</span><span class="sxs-lookup"><span data-stu-id="d21a9-154">This is done by calling [**IWMDRMReader::CancelLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancellicenseacquisition).</span></span> <span data-ttu-id="d21a9-155">Chamar esse método enviará um evento de **\_ \_ licença de aquisição WMT** com um valor **HRESULT** de aquisição de DRM do NS \_ S \_ \_ \_ cancelado.</span><span class="sxs-lookup"><span data-stu-id="d21a9-155">Calling this method will send a **WMT\_ACQUIRE\_LICENSE** event with an **HRESULT** value of NS\_S\_DRM\_ACQUIRE\_CANCELLED.</span></span>

<span data-ttu-id="d21a9-156">Se o **HR** for igual à licença do NS \_ S \_ DRM \_ \_ adquirida, a licença será adquirida e o aplicativo poderá tentar reproduzir o arquivo ou copiá-lo para um dispositivo ou executar qualquer ação à qual ele tenha solicitado direitos.</span><span class="sxs-lookup"><span data-stu-id="d21a9-156">If **hr** equals NS\_S\_DRM\_LICENSE\_ACQUIRED, then the license has been acquired and the application can attempt to play the file, or copy it to a device or perform whatever action it had requested rights for.</span></span>

<span data-ttu-id="d21a9-157">No Windows XP, um novo código de erro foi introduzido: \_ licença NS E \_ DRM não \_ \_ adquirida.</span><span class="sxs-lookup"><span data-stu-id="d21a9-157">On Windows XP, a new error code was introduced: NS\_E\_DRM\_LICENSE\_NOTACQUIRED.</span></span> <span data-ttu-id="d21a9-158">Esse código de erro é gerado sempre que os componentes de tempo de execução do formato do Windows Media no Windows XP falham ao adquirir uma licença durante a aquisição de licença silenciosa ou não silenciosa.</span><span class="sxs-lookup"><span data-stu-id="d21a9-158">This error code is generated whenever the Windows Media Format run-time components on Windows XP fail to acquire a license during silent or non-silent license acquisition.</span></span> <span data-ttu-id="d21a9-159">Em outras plataformas, o \_ erro de armazenamento de licença do NS E \_ DRM \_ \_ \_ geralmente é retornado quando a aquisição de licença falha.</span><span class="sxs-lookup"><span data-stu-id="d21a9-159">On other platforms, NS\_E\_DRM\_LICENSE\_STORE\_ERROR is usually returned when license acquisition fails.</span></span> <span data-ttu-id="d21a9-160">O novo código de erro destina-se a distinguir a falha de aquisição de licença de outras condições de falha em que o erro de armazenamento de licença do NS \_ E \_ DRM \_ \_ \_ é gerado.</span><span class="sxs-lookup"><span data-stu-id="d21a9-160">The new error code is intended to distinguish license acquisition failure from other failure conditions where NS\_E\_DRM\_LICENSE\_STORE\_ERROR is generated.</span></span>

<span data-ttu-id="d21a9-161">A maneira recomendada para lidar com esses erros quando eles são retornados após uma tentativa de aquisição de licença silenciosa é mostrada no seguinte trecho de código:</span><span class="sxs-lookup"><span data-stu-id="d21a9-161">The recommended way to handle these errors when they are returned after a silent license acquisition attempt is shown in the following code snippet:</span></span>


```C++
if( hrStatus == NS_E_DRM_LICENSE_NOTACQUIRED || 
    hrStatus == NS_E_DRM_LICENSE_STORE_ERROR )
{
  // Attempt non-silent license acquisition.
}
else if( hrStatus == NS_E_DRM_NEEDS_INDIVIDUALIZATION )
{
  // Individualize and then retry.
}
else if( FAILED(hrStatus) )
{
  // Display a helpful error message.
}
else
{
  // Success. Play content.
}
```



> [!Note]  
> <span data-ttu-id="d21a9-162">O DRM não é compatível com a versão baseada em x64 deste SDK.</span><span class="sxs-lookup"><span data-stu-id="d21a9-162">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d21a9-163">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d21a9-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d21a9-164">**Lendo arquivos protegidos**</span><span class="sxs-lookup"><span data-stu-id="d21a9-164">**Reading Protected Files**</span></span>](reading-protected-files.md)
</dt> </dl>

 

 




