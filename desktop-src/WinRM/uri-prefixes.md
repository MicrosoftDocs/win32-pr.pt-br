---
title: Prefixos de URI
description: O prefixo do URI de recurso é diferente dependendo de qual esquema XML descreve o recurso.
ms.assetid: 47c32da6-98c9-4f66-82ac-647976127cb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b44744d7ac7d158bd7d00423396681fef1499c94d61b5cb74a1dee48dad5c784
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898666"
---
# <a name="uri-prefixes"></a>Prefixos de URI

O prefixo do [*URI de recurso*](windows-remote-management-glossary.md) é diferente dependendo de qual esquema XML descreve o recurso.

## <a name="prefixes"></a>Prefixos

Se você acessar uma classe [*cim*](windows-remote-management-glossary.md) 2,1, como o [**\_ DataFile do CIM**](/windows/desktop/CIMWin32Prov/cim-datafile), o prefixo do URI será diferente do prefixo de uma classe CIM 2,9, como o **CIM \_ AdminDomain**. as classes cim 2,1 são documentadas na seção [classes cim](/windows/desktop/WmiSdk/cimclas) de Instrumentação de Gerenciamento do Windows (WMI).

A maioria das [classes WMI](/windows/desktop/WmiSdk/wmi-classes) está no namespace WMI **\\ cimv2 raiz** . As classes para o provedor de [IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)(interface de gerenciamento de plataforma inteligente) da Microsoft estão em **\\ hardware raiz**.

A lista a seguir contém os prefixos de URI de recurso para esses esquemas:

-   Classes WMI ou CIM 2,1 no namespace **raiz \\ cimv2**

    "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/"

-   Classes CIM 2,9 ou classes IPMI

    "https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2"

-   Maneira alternativa de acessar classes de provedor de IPMI

    "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/hardware/"

Para obter mais informações, consulte [URIs de recurso](resource-uris.md) e [cadeias de caracteres URLPrefix](/windows/desktop/Http/urlprefix-strings). para obter mais informações sobre como gerar um URI para uma classe ou um método WMI, consulte [Gerenciamento Remoto do Windows e WMI](windows-remote-management-and-wmi.md).

## <a name="prefix-aliases"></a>Aliases de prefixo

Um alias de prefixo é um atalho que representa o prefixo de URI de recurso longo. Você também pode usar aliases na linha de comando do **WinRM** . Para exibir uma lista de aliases disponíveis, digite **aliases de ajuda do WinRM**.

Lembre-se de que um alias não pode ser usado dentro de uma referência de ponto de extremidade (EPR) ao especificar um URI de recurso. Windows O gerenciamento remoto não pode expandir o alias quando ele é inserido em XML.

No exemplo de código a seguir, o alias do WinRM é usado em um EPR em vez do URI de recurso completo, que é `http://schemas.microsoft.com/wbem/wsman/1/config/Listener` . Nesse caso, o WinRM retorna um erro que indica que o serviço não pode processar a solicitação.


```XML
ResourceUri = "</wxf:ResourceCreated>.....
<w:ResourceURI>winrm/config/listener</w:ResourceURI>...
</w:SelectorSet></a:ReferenceParameters></wxf:ResourceCreated>"

Set ResourceLocator = WSManObj.CreateResourceLocator(resourceUri)
ResponseStr = Session.Get(ResourceLocator, 0)
```



As listas a seguir definem aliases e URIs de recursos para os quais substituem.

<dl> <dt>

<span id="wmi"></span><span id="WMI"></span>esses
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi`

</dd> <dt>

<span id="wmicimv2"></span><span id="WMICIMV2"></span>wmicimv2
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2`

</dd> <dt>

<span id="cimv2"></span><span id="CIMV2"></span>cimv2
</dt> <dd>

`https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2`

</dd> <dt>

<span id="winrm"></span><span id="WINRM"></span>WinRM
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span id="wsman"></span><span id="WSMAN"></span>WSMan
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span id="shell"></span><span id="SHELL"></span>Shell
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/windows/shell`

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[sobre Gerenciamento Remoto do Windows](about-windows-remote-management.md)
</dt> <dt>

[Windows Gerenciamento remoto e WMI](windows-remote-management-and-wmi.md)
</dt> <dt>

[URIs do Recurso](resource-uris.md)
</dt> </dl>
