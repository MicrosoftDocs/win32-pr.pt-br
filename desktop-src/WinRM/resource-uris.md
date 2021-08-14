---
title: URIs do Recurso
description: Um URI de recurso é um identificador para um tipo distinto de operação de gerenciamento ou valor usado pelos serviços de gerenciamento que implementam o protocolo de WS-Management.
ms.assetid: 478a6e5d-0675-462e-b2fd-fd2b5379e298
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93f13e18abd7ea452b84043dfef3d6bf6b18be6c476c0dfff9a34e42e45dbc14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323718"
---
# <a name="resource-uris"></a>URIs do Recurso

Um [*URI de recurso*](windows-remote-management-glossary.md) é um identificador para um tipo distinto de operação de gerenciamento ou valor usado pelos serviços de gerenciamento que implementam o protocolo de WS-Management. Um valor de gerenciamento pode ser a temperatura dentro de um computador. Um exemplo de uma operação de gerenciamento é iniciar um serviço interrompido ou definir uma cota de usuário de volume de disco.

## <a name="resource-uri-format"></a>Formato do URI de recurso

Um URI consiste em um prefixo e um caminho para um recurso, como é mostrado no exemplo a seguir:

"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_LogicalDisk"

Essa especificação de esquema indica que o URI é baseado na versão 1 do protocolo WS-Management oficial e que o recurso é um [**\_ LogicalDisk Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) no namespace "raiz \\ cimv2" do repositório do WMI. Os prefixos de URI contêm uma especificação de esquema, como "schemas.microsoft.com/wbem/wsman/1/wmi" e um tipo específico de recurso, como o **\_ LogicalDisk do Win32**. para obter mais informações sobre como identificar uma instância específica de uma classe WMI, consulte [Gerenciamento Remoto do Windows e WMI](windows-remote-management-and-wmi.md).

Para obter mais informações, consulte [prefixos de URI](uri-prefixes.md).

## <a name="types-of-resource-uris"></a>Tipos de URIs de recurso

embora [*Instrumentação de Gerenciamento do Windows (WMI)*](windows-remote-management-glossary.md) seja a principal fonte de dados de gerenciamento para sistemas operacionais baseados em Windows, outras fontes de esquema de gerenciamento também existem.

a lista a seguir descreve vários tipos de URIs de recursos usados pelo Gerenciamento Remoto do Windows:

-   URIs de WMI

    Esse grupo de URIs representa um [*modelo CIM*](/windows/desktop/WmiSdk/gloss-c) caminho de classe que inclui o namespace e a classe.

    Os URIs do WMI podem ser usados em:

    -   Métodos de [**sessão**](session.md)
    -   Métodos [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
    -   Métodos [**WSMan. CreateResourceLocator**](wsman-createresourcelocator.md) ou [**IWSMan. CreateResourceLocator**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator)
    -   Métodos [**ResourceLocator**](resourcelocator.md) ou [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)

-   URIs IPMI

    Esse grupo de URIs representa URIs padrão do setor baseados na versão 2,9 do CIM. URIs IPMI podem ser usados em métodos de [**sessão**](session.md) [**Get**](session-get.md), [**Put**](session-put.md), [**Enumerate**](session-enumerate.md) e [**Invoke**](session-invoke.md).

    Um exemplo é https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2/CIM_NumericSensor.xsd. Esse recurso é definido de acordo com o esquema CIM [DMTF.org](https://www.dmtf.org/home) .

-   URIs de configuração do WinRM

    Esse grupo de URIs são operações de configuração para a configuração do [*ouvinte*](windows-remote-management-glossary.md) do WinRM.

    https://schemas.microsoft.com/wbem/wsman/1/config/listener pode ser usado em métodos de [**sessão**](session.md) [**Get**](session-get.md), [**Put**](session-put.md), [**Create**](session-create.md), [**delete**](session-delete.md)e [**Enumerate**](session-enumerate.md).

-   URIs de SEL ( [*log de eventos do sistema*](windows-remote-management-glossary.md) )

    Esse grupo de URIs assina eventos do coletor de eventos do BMC. Você pode assinar esses eventos usando a ferramenta de linha de comando **wevtutil** . Para obter mais informações, consulte https://schemas.microsoft.com/wbem/wsman/1/logrecord/sel.

## <a name="case-sensitivity"></a>Diferenciação de maiúsculas e minúsculas

O [*plug-in WMI*](windows-remote-management-glossary.md) preserva o caso do URI de recurso recebido em uma solicitação. No entanto, para garantir a interoperabilidade com outras implementações do protocolo WS-Management, use o caso correto para o recurso solicitado no URI de recurso. O caso correto é a ortografia definida pelo provedor de recursos.

Enquanto os URIs de recurso não exigem diferenciação de maiúsculas e minúsculas, o [*fragmento*](windows-remote-management-glossary.md) XML faz. Um fragmento especifica apenas uma propriedade, em vez de todo o conjunto de propriedades de um recurso. No caso de recursos do WMI, a sintaxe do fragmento Obtém uma propriedade de uma instância de recurso. Por exemplo, obter apenas a propriedade **version** de [**\_ OperatingSystem do Win32**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) requer o uso de um fragmento. para obter mais informações sobre fragmentos, consulte "adicionando um seletor a um objeto ResourceLocator ou IWSManResourceLocator" em [Gerenciamento Remoto do Windows e WMI](windows-remote-management-and-wmi.md).

Seguindo os padrões de XML e [*XPath*](windows-remote-management-glossary.md) , o [*plug-in do WMI*](windows-remote-management-glossary.md) impõe a diferenciação de maiúsculas e minúsculas para fragmentos e XML que definem os parâmetros de entrada para um método. Diferenciar maiúsculas de minúsculas é necessário para dar suporte ao padrão XPath 1.0/nível 1. Para obter dados WMI por meio do WinRM, a diferenciação de maiúsculas e minúsculas significa que os nomes de classes, propriedades e métodos WMI devem corresponder ao caso do nome encontrado no repositório WMI.

Para obter mais informações, consulte [Sintaxe XPath](/previous-versions/dotnet/netframework-4.0/ms256471(v=vs.100)).

## <a name="case-sensitivity-examples"></a>Exemplos de sensibilidade de caso

Por exemplo, um script que obtém a propriedade **de \_ descritor de segurança** de uma instância da classe de [**\_ serviço WMI Win32**](/windows/desktop/CIMWin32Prov/win32-service) não pode usar maiúsculas para os nomes no caminho do fragmento, somente o URI. O [*plug-in do WMI*](windows-remote-management-glossary.md) do WinRM retorna um erro para o seguinte exemplo de VBScript porque o XML do XPath fornecido para o **FragmentPath** não usa o caso correto. No repositório WMI, a classe é escrita "serviço Win32 \_ ".


```VB
RResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_& "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_SERVICE/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



A seguinte versão do mesmo exemplo mostra o uso correto do caso para a classe [**de \_ serviço do Win32**](/windows/desktop/CIMWin32Prov/win32-service) e a propriedade do **\_ descritor de segurança** .


```VB
ResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_Service/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[sobre Gerenciamento Remoto do Windows](about-windows-remote-management.md)
</dt> <dt>

[Gerenciamento de hardware remoto](remote-hardware-management.md)
</dt> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 