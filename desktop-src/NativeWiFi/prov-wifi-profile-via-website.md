---
title: Provisionar um perfil de Wi-Fi por meio de um site
description: Permita que os usuários baixem um perfil de um site e provisione-os.
ms.topic: article
ms.date: 01/22/2020
ms.openlocfilehash: e34c83fbee100316256293e27eac96dae685c37d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917651"
---
# <a name="provision-a-wi-fi-profile-via-a-website"></a>Provisionar um perfil de Wi-Fi por meio de um site

O fluxo de trabalho descrito neste tópico foi introduzido no Windows 10, versão 2004. Este tópico mostra como configurar um site para que um usuário possa provisionar um perfil para uma rede Passpoint (ou para uma rede normal) antes de passar para o intervalo dos pontos de acesso Wi-Fi correspondentes. Um cenário de exemplo é que de um usuário que pode estar planejando visitar um aeroporto ou uma conferência pela primeira vez, e quer se preparar antecipadamente baixando e provisionando um perfil em casa.

Como desenvolvedor, você habilita o fluxo de trabalho fornecendo um perfil XML e configurando um site. Os usuários podem, então, provisionar um perfil de Wi-Fi baixando-o de seu site por meio de um navegador da Web. No dispositivo do usuário, o perfil de Wi-Fi é provisionado usando a ativação de URI e o aplicativo de **configurações** do Windows.

Este fluxo de trabalho substitui o mecanismo no Internet Explorer para provisionar Wi-Fi perfis, que se baseiam em APIs JavaScript específicas da Microsoft. Esse novo fluxo de trabalho deve funcionar com todos os principais navegadores.

## <a name="the-workflow-in-more-detail"></a>O fluxo de trabalho em mais detalhes

Você pode ativar este fluxo de trabalho de um hiperlink que inclui como um argumento o URI de download do documento XML de provisionamento.

```xml
ms-settings:wifi-provisioning?uri={download_uri}
```

Por exemplo, a marcação HTML a seguir fornece um link para instalar os perfis encontrados em um documento hipotético `http://contoso.com/ProvisioningDoc.xml` .

```html
<a href="ms-settings:wifi-provisioning?uri=http://contoso.com/ProvisioningDoc.xml">Install</a>
```

O XML deve aderir ao esquema de provisionamento (consulte [provisionamento de conta](/windows-hardware/drivers/mobilebroadband/account-provisioning)). O XML também deve incluir um ou mais elementos [WLANProfile](./wlan-profileschema-wlanprofile-element.md)   .Cada perfil será exibido na caixa de diálogo **Adicionar** descrita em Avançar.

Quando o usuário clica no link HTML, o fluxo de trabalho de instalação é invocado no aplicativo **configurações** . O documento XML de provisionamento é baixado pelo aplicativo **configurações** . Depois de baixado, são exibidas informações sobre os perfis, a assinatura e o assinante (desde que o documento esteja de acordo com o esquema).

![O aplicativo configurações](images/install-dialog.png)

O botão **Adicionar** na caixa de diálogo no aplicativo **configurações** será habilitado somente se o arquivo de provisionamento for assinado e confiável.

## <a name="in-your-web-page-determine-whether-this-workflow-is-supported"></a>Na página da Web, determine se há suporte para esse fluxo de trabalho

Não há nenhuma maneira em JavaScript determinar a versão de Build exata do Windows. Mas se o usuário estiver usando o navegador da Web Microsoft Edge, você poderá determinar a versão do Edge inspecionando o valor do `User-agent` cabeçalho http. Se a versão for maior ou igual a `18.nnnnn` , o fluxo de trabalho terá suporte.

## <a name="related-topics"></a>Tópicos relacionados

* [Provisionamento de conta](/windows-hardware/drivers/mobilebroadband/account-provisioning)
* [Elemento WLANProfile](./wlan-profileschema-wlanprofile-element.md)