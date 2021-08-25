---
title: Manipulando eventos de aquisição de licença
description: Manipulando eventos de aquisição de licença
ms.assetid: e118bf09-1fa6-41b6-a6bb-3e8cb6097994
keywords:
- Windows SDK de Formato de Mídia, manipulando eventos de aquisição de licença
- Windows SDK de Formato de Mídia, eventos de aquisição de licença
- FORMATO DE SISTEMAS Avançados (ASF), manipulando eventos de aquisição de licença
- ASF (Formato de Sistemas Avançados), manipulando eventos de aquisição de licença
- FORMATO DE SISTEMAS Avançados (ASF), eventos de aquisição de licença
- ASF (Formato de Sistemas Avançados), eventos de aquisição de licença
- DRM (gerenciamento de direitos digitais), manipulando eventos de aquisição de licença
- DRM (gerenciamento de direitos digitais), manipulação de eventos de aquisição de licença
- DRM (gerenciamento de direitos digitais), eventos de aquisição de licença
- DRM (gerenciamento de direitos digitais), eventos de aquisição de licença
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7eab9afe85d4e58ae422134e5268c5b411058cf5048f774994b0cc02b173fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006706"
---
# <a name="handling-license-acquisition-events"></a>Manipulando eventos de aquisição de licença

Um aplicativo de leitor habilitado para DRM, em seu método de retorno de chamada [**IWMStatusCallback::OnStatus,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) lida com os quatro eventos a seguir relacionados ao processo de aquisição de licença:

-   **ESTADO DE ASSINATURA DO WMT \_ LICENSEURL \_ \_**
-   **WMT \_ SEM \_ DIREITOS**
-   **WMT \_ NO \_ RIGHTS \_ EX**
-   **LICENÇA DE \_ AQUISIÇÃO DO WMT \_**

**ESTADO DE ASSINATURA DO WMT \_ LICENSEURL \_ \_**

Quando o componente DRM detecta o conteúdo protegido pelo DRM versão 7, ele primeiro procura uma licença válida no sistema local. Se nenhum existir, ele avaliará a URL de aquisição de licença no título DRM do arquivo e enviará um evento **WMT \_ LICENSEURL \_ SIGNATURE \_ STATE** com *pValue* definido como um dos valores DE CONFIANÇA [**\_ DRMLA \_ DO WMT,**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust) indicando se a URL é confiável, não confiável ou foi adulterada. Se a URL não for confiável, o aplicativo deverá avisar o usuário. Se a URL tiver sido adulterada, o arquivo deverá ser considerado corrompido e o aplicativo não deverá navegar até a URL sem emite um aviso forte do usuário.

**WMT \_ SEM \_ DIREITOS**

O **evento WMT \_ NO \_ RIGHTS** é enviado somente para o conteúdo da versão 1 do DRM, o que significa que a licença deve ser adquirida de forma silenciosa. Em outras palavras, o usuário deve navegar até uma página da Web para adquirir uma licença. A URL da página é recuperada como uma cadeia de caracteres com terminação nula de caractere largo do parâmetro *pValue* no **método OnStatus.**

Se apropriado, um aplicativo pode facilitar para o usuário navegar até a página da Web, seja abrindo Internet Explorer em um processo separado ou hospedando o controle navegador da Web. No entanto, isso não é necessário. No mínimo, um aplicativo pode simplesmente exibir a URL para o usuário em uma caixa de mensagem e solicitar que ele a colar na barra de endereços Internet Explorer. O exemplo audioplayer demonstra a manipulação adequada do evento **WMT \_ NO \_ RIGHTS,** incluindo como formatar a cadeia de caracteres de URL e como usar o **método CreateProcess** para abrir o Internet Explorer e navegar até a URL especificada.

Como o aplicativo não tem como saber quando uma licença drm versão 1 foi adquirida, é responsabilidade do usuário tentar abrir o arquivo novamente depois de adquirir a licença.

Esse mesmo processo de aquisição de licença não silenciosa também pode ser usado para licenças da versão 7, mas nesse caso, o aplicativo pode primeiro chamar [**IWMDRMReader::MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition). Esse método fará com que o armazenamento de licenças local seja verificado repetidamente até que a licença do novo arquivo seja encontrada. Nesse ponto, o aplicativo receberá um evento **WMT \_ ACQUIRE \_ LICENSE.** Para todas as licenças da versão 7, é recomendável que os aplicativos deem aos usuários a opção de obter licenças silenciosamente ou não silenciosamente.

**WMT \_ NO \_ RIGHTS \_ EX**

O **evento WMT \_ NO RIGHTS \_ \_ EX** indica que o conteúdo é protegido pelo DRM versão 7 e, portanto, o processo de aquisição de licença pode continuar silenciosa ou não silenciosamente. Em geral, a aquisição de licença silenciosa é mais conveniente para os usuários finais, embora algumas pessoas prefiram adquirir todas as licenças de forma silenciosa. Quando a aquisição de licença exige que o usuário envie informações pessoais ou de pagamento, o processo sempre deve ser executado de forma não silenciosa. A aquisição de licença não silenciosa é descrita acima no **título WMT \_ NO \_ RIGHTS.** A aquisição silenciosa continua da seguinte forma:

1.  Caste *o parâmetro pValue* em uma estrutura [**WM GET LICENSE \_ \_ \_ DATA**](wm-get-license-data.md) e armazene a estrutura caso ela seja necessária posteriormente para aquisição de licença não silenciosa.
2.  Chame **QueryInterface** no objeto de leitor para obter a interface [**IWMDRMReader.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
3.  Chame [**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) e especifique 0x1 no parâmetro *dwFlags* para indicar a aquisição silenciosa de idioma. Essa é uma chamada assíncrona que retorna imediatamente.
4.  Aguarde o evento **WMT \_ ACQUIRE \_ LICENSE.**

**LICENÇA DE \_ AQUISIÇÃO DO WMT \_**

O **evento WMT \_ ACQUIRE \_ LICENSE** é enviado depois que o processo de aquisição de licença é concluído para uma licença drm versão 7. [**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) faz com que esse evento seja enviado para aquisição silenciosa e [**MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition) faz com que ele seja enviado para aquisição não silenciosa. No manipulador de eventos, caste *pValue* em um ponteiro  para uma estrutura [**WM GET \_ LICENSE \_ \_ DATA**](wm-get-license-data.md) e examine o membro de rh para determinar se a licença foi adquirida com êxito. Se **o rh** for igual a NS E \_ DRM NO RIGHTS, isso indicará que a licença deve ser adquirida \_ de forma não \_ \_ silenciosa. Os aplicativos devem permitir que os usuários cancelem o processo de aquisição de licença a qualquer momento. Isso é feito chamando [**IWMDRMReader::CancelLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancellicenseacquisition). Chamar esse método enviará um **evento WMT \_ ACQUIRE \_ LICENSE** com um **valor HRESULT** de NS \_ S \_ DRM ACQUIRE \_ \_ CANCELLED.

Se **hr** for igual a NS \_ S \_ DRM LICENSE \_ ACQUIRED, a licença foi adquirida e o aplicativo poderá tentar reproduzir o arquivo ou copiá-lo para um dispositivo ou executar qualquer ação para a qual ele solicitou \_ direitos.

No Windows XP, um novo código de erro foi introduzido: NS \_ E \_ DRM \_ LICENSE \_ NOTACQUIRED. Esse código de erro é gerado sempre que os componentes de tempo de Windows de tempo de Windows no Windows XP falham ao adquirir uma licença durante a aquisição de licença silenciosa ou não silenciosa. Em outras plataformas, o ERRO DO ARMAZENAMENTO DE LICENÇAS \_ NS E \_ DRM \_ geralmente é retornado quando a \_ \_ aquisição de licença falha. O novo código de erro destina-se a distinguir a falha de aquisição de licença de outras condições de falha em que nS \_ E \_ DRM \_ LICENSE STORE ERROR \_ é \_ gerado.

A maneira recomendada de tratar esses erros quando eles são retornados após uma tentativa de aquisição de licença silenciosa é mostrada no snippet de código a seguir:


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
> O DRM não é suportado pela versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Lendo arquivos protegidos**](reading-protected-files.md)
</dt> </dl>

 

 




