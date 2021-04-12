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
# <a name="handling-license-acquisition-events"></a>Lidando com eventos de aquisição de licença

Um aplicativo de leitor habilitado para DRM, em seu método de retorno de chamada [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) , lida com os quatro eventos a seguir relacionados ao processo de aquisição de licença:

-   **\_estado de \_ assinatura WMT LICENSEURL \_**
-   **WMT \_ sem \_ direitos**
-   **WMT \_ sem \_ direitos \_ ex**
-   **\_licença de aquisição do WMT \_**

**\_estado de \_ assinatura WMT LICENSEURL \_**

Quando o componente DRM detecta conteúdo protegido pelo DRM versão 7, ele primeiro procura uma licença válida no sistema local. Se não houver nenhum, ele avaliará a URL de aquisição de licença no cabeçalho DRM do arquivo e enviará um evento de **estado de \_ \_ assinatura \_ WMT LICENSEURL** *com uma* definição de valor para um dos valores de [**\_ \_ confiança WMT DRMLA**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust) , indicando se a URL é confiável, não confiável ou se foi violada. Se a URL não for confiável, o aplicativo deverá avisar o usuário. Se a URL tiver sido violada, o arquivo deverá ser considerado corrompido e o aplicativo não deverá navegar até a URL sem emitir um aviso forte ao usuário.

**WMT \_ sem \_ direitos**

O evento **WMT \_ nenhum \_ Rights** é enviado somente para conteúdo DRM versão 1, o que significa que a licença deve ser adquirida não silenciosamente. Em outras palavras, o usuário deve navegar para uma página da Web para adquirir uma licença. A URL da página é recuperada como uma cadeia de caracteres terminada em nulo de caractere largo *do parâmetro de número de espaço* no método **OnStatus** .

Se apropriado, um aplicativo pode facilitar para o usuário navegar até a página da Web, seja abrindo o Internet Explorer em um processo separado ou hospedando o controle do navegador da Web. No entanto, isso não é necessário. Na pior das hipóteses, um aplicativo pode simplesmente exibir a URL para o usuário em uma caixa de mensagem e pedir para colá-la na barra de endereços do Internet Explorer. O exemplo AudioPlayer demonstra o tratamento adequado do evento **WMT \_ no \_ Rights** , incluindo como formatar a cadeia de caracteres da URL e como usar o método **CreateProcess** para abrir o Internet Explorer e navegar até a URL especificada.

Como o aplicativo não tem como saber quando uma licença do DRM versão 1 foi adquirida, cabe ao usuário tentar abrir o arquivo novamente após adquirir a licença.

Esse mesmo processo de aquisição de licença não silenciosa também pode ser usado para licenças da versão 7, mas, nesse caso, o aplicativo pode primeiro chamar [**IWMDRMReader:: MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition). Esse método fará com que o repositório de licenças local seja verificado repetidamente até que a licença do novo arquivo seja encontrada. Nesse ponto, o aplicativo receberá um evento **de \_ \_ licença de aquisição WMT** . Para todas as licenças da versão 7, é recomendável que os aplicativos forneçam aos usuários a opção de obter licenças silenciosamente ou não silenciosamente.

**WMT \_ sem \_ direitos \_ ex**

O evento **WMT \_ no \_ Rights \_ ex** indica que o conteúdo está protegido pelo DRM versão 7 e, portanto, o processo de aquisição de licença pode continuar silenciosamente ou não silenciosamente. Em geral, a aquisição de licença silenciosa é mais conveniente para os usuários finais, embora algumas pessoas prefiram adquirir todas as licenças não silenciosamente. Quando a aquisição de licença exige que o usuário envie pagamentos ou informações pessoais, o processo sempre deve ser executado de forma não silenciosa. A aquisição de licença não silenciosa é descrita acima no cabeçalho **WMT \_ nenhum \_ direito** . A aquisição silenciosa continua da seguinte maneira:

1.  Converta *o parâmetro de chegar a uma* estrutura de [**\_ \_ \_ dados obter licença do WM**](wm-get-license-data.md) e armazene a estrutura caso ela seja necessária posteriormente para aquisição de licença não silenciosa.
2.  Chame **QueryInterface** no objeto Reader para obter a interface [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) .
3.  Chame [**IWMDRMReader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) e especifique 0x1 no parâmetro *dwFlags* para indicar a aquisição de linguagem silenciosa. Essa é uma chamada assíncrona que retorna imediatamente.
4.  Aguarde o evento **de \_ \_ licença de aquisição WMT** .

**\_licença de aquisição do WMT \_**

O evento de **\_ \_ licença de aquisição WMT** é enviado após a conclusão do processo de aquisição de licença para uma licença do DRM versão 7. [**IWMDRMReader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) faz com que esse evento seja enviado para aquisição silenciosa e [**MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition) faz com que ele seja enviado para aquisição não silenciosa. No manipulador de eventos, converta a um *ponteiro para uma* estrutura de [**\_ \_ \_ dados obter licença do WM**](wm-get-license-data.md) e examine o membro de **RH** para determinar se a licença foi adquirida com êxito. Se **HR** for igual a NS \_ E \_ DRM \_ sem \_ direitos, isso indica que a licença deve ser adquirida não silenciosamente. Os aplicativos devem permitir que os usuários cancelem o processo de aquisição de licença a qualquer momento. Isso é feito chamando [**IWMDRMReader:: CancelLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancellicenseacquisition). Chamar esse método enviará um evento de **\_ \_ licença de aquisição WMT** com um valor **HRESULT** de aquisição de DRM do NS \_ S \_ \_ \_ cancelado.

Se o **HR** for igual à licença do NS \_ S \_ DRM \_ \_ adquirida, a licença será adquirida e o aplicativo poderá tentar reproduzir o arquivo ou copiá-lo para um dispositivo ou executar qualquer ação à qual ele tenha solicitado direitos.

No Windows XP, um novo código de erro foi introduzido: \_ licença NS E \_ DRM não \_ \_ adquirida. Esse código de erro é gerado sempre que os componentes de tempo de execução do formato do Windows Media no Windows XP falham ao adquirir uma licença durante a aquisição de licença silenciosa ou não silenciosa. Em outras plataformas, o \_ erro de armazenamento de licença do NS E \_ DRM \_ \_ \_ geralmente é retornado quando a aquisição de licença falha. O novo código de erro destina-se a distinguir a falha de aquisição de licença de outras condições de falha em que o erro de armazenamento de licença do NS \_ E \_ DRM \_ \_ \_ é gerado.

A maneira recomendada para lidar com esses erros quando eles são retornados após uma tentativa de aquisição de licença silenciosa é mostrada no seguinte trecho de código:


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
> O DRM não é compatível com a versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Lendo arquivos protegidos**](reading-protected-files.md)
</dt> </dl>

 

 




