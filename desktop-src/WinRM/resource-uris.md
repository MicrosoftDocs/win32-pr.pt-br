---
title: URIs do Recurso
description: Um URI de recurso é um identificador para um tipo distinto de operação de gerenciamento ou valor usado pelos serviços de gerenciamento que implementam o WS-Management protocolo.
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

Um [*URI de recurso*](windows-remote-management-glossary.md) é um identificador para um tipo distinto de operação de gerenciamento ou valor usado pelos serviços de gerenciamento que implementam o WS-Management protocolo. Um valor de gerenciamento pode ser a temperatura dentro de um computador. Um exemplo de uma operação de gerenciamento é iniciar um serviço parado ou definir uma cota de usuário do volume de disco.

## <a name="resource-uri-format"></a>Formato de URI do recurso

Um URI consiste em um prefixo e um caminho para um recurso, conforme mostrado no exemplo a seguir:

"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_LogicalDisk"

Essa especificação de esquema indica que o URI é baseado na versão 1 do protocolo WS-Management oficial e que o recurso é um [**\_ LogicalDisk win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) no namespace "root cimv2" do repositório \\ WMI. Os prefixos de URI contêm uma especificação de esquema, como "schemas.microsoft.com/wbem/wsman/1/wmi" e um tipo específico de recurso, como **Win32 \_ LogicalDisk.** Para obter mais informações sobre como identificar uma instância específica de uma classe WMI, consulte Windows Gerenciamento Remoto [e WMI](windows-remote-management-and-wmi.md).

Para obter mais informações, consulte [Prefixos de URI](uri-prefixes.md).

## <a name="types-of-resource-uris"></a>Tipos de URIs de recurso

Embora [*Windows WMI (Instrumentação*](windows-remote-management-glossary.md) de Gerenciamento) seja a principal fonte de dados de gerenciamento para sistemas operacionais baseados em Windows, outras fontes de esquema de gerenciamento também existem.

A lista a seguir descreve vários tipos de URIs de recurso usados pelo Windows Gerenciamento Remoto:

-   WMI URIs

    Esse grupo de URIs representa um [*caminho modelo CIM*](/windows/desktop/WmiSdk/gloss-c) classe que inclui namespace e classe.

    UrIs WMI podem ser usados em:

    -   [**Métodos**](session.md) de sessão
    -   [**Métodos IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
    -   [**Métodos WSMan.CreateResourceLocator**](wsman-createresourcelocator.md) [**ou IWSMan.CreateResourceLocator**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator)
    -   [**Métodos ResourceLocator**](resourcelocator.md) [**ou IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)

-   IPMI URIs

    Esse grupo de URIs representa URIs padrão do setor com base na versão CIM 2.9. URIs IPMI podem ser usados em [**Métodos**](session.md) de sessão [**Get,**](session-get.md) [**Put,**](session-put.md) [**Enumerate**](session-enumerate.md) e [**Invoke**](session-invoke.md).

    Um exemplo é https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2/CIM_NumericSensor.xsd. Esse recurso é definido de acordo com o [DMTF.org](https://www.dmtf.org/home) esquema CIM.

-   URIs de configuração do WinRM

    Esse grupo de URIs são operações de configuração para a configuração do [*ouvinte WinRM.*](windows-remote-management-glossary.md)

    https://schemas.microsoft.com/wbem/wsman/1/config/listener pode ser usado nos [**métodos de**](session.md) sessão [**Get,**](session-get.md) [**Put,**](session-put.md) [**Create,**](session-create.md) [**Delete**](session-delete.md)e [**Enumerate**](session-enumerate.md).

-   URIs [*do SEL (Log*](windows-remote-management-glossary.md) de Eventos do Sistema)

    Esse grupo de URIs assina eventos do Coletor de Eventos do BMC. Você pode assinar esses eventos usando a ferramenta de linha de comando **Wevtutil.** Para obter mais informações, consulte https://schemas.microsoft.com/wbem/wsman/1/logrecord/sel.

## <a name="case-sensitivity"></a>Diferenciação de maiúsculas e minúsculas

O [*plug-in WMI*](windows-remote-management-glossary.md) preserva o caso do URI de recurso recebido em uma solicitação. No entanto, para garantir a interoperabilidade com outras implementações do protocolo WS-Management, use o caso correto para o recurso solicitado no URI do recurso. O caso correto é a ortografia definida pelo provedor de recursos.

Embora os URIs de recurso não exigem a sensibilidade a caso, [*o*](windows-remote-management-glossary.md) XML de fragmento requer. Um fragmento especifica apenas uma propriedade, em vez de todo o conjunto de propriedades para um recurso. No caso de recursos WMI, a sintaxe de fragmento obtém uma propriedade de uma instância de recurso. Por exemplo, obter apenas a **propriedade Version** de [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) requer o uso de um fragmento. Para obter mais informações sobre fragmentos, consulte "Adicionando um seletor a um objeto ResourceLocator ou IWSManResourceLocator" no [Windows Remote Management e WMI](windows-remote-management-and-wmi.md).

Seguindo os padrões XML e [*XPath,*](windows-remote-management-glossary.md) o [*plug-in WMI*](windows-remote-management-glossary.md) impõe a sensibilidade de caso para fragmentos e XML que define os parâmetros de entrada para um método. A sensibilidade a caso é necessária para dar suporte ao padrão XPath 1.0/Nível 1. Para obter dados WMI por meio do WinRM, a sensibilidade a caso significa que os nomes de classes, propriedades e métodos WMI devem corresponder ao caso do nome encontrado no repositório WMI.

Para obter mais informações, consulte [Sintaxe XPath](/previous-versions/dotnet/netframework-4.0/ms256471(v=vs.100)).

## <a name="case-sensitivity-examples"></a>Exemplos de sensibilidade a casos

Por exemplo, um script que obtém a propriedade **SECURITY \_ DESCRIPTOR** de uma instância da classe WMI [**Win32 \_ Service**](/windows/desktop/CIMWin32Prov/win32-service) não pode usar maiúsculas para os nomes no caminho do fragmento, somente o URI. O [*plug-in WMI*](windows-remote-management-glossary.md) do WinRM retorna um erro para o exemplo de VBScript a seguir porque o XML XPath fornecido para **o FragmentPath** não usa o caso correto. No repositório WMI, a classe é escrita "Serviço \_ Win32".


```VB
RResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_& "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_SERVICE/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



A versão a seguir do mesmo exemplo mostra o uso correto de case para a classe de serviço [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-service) e a **propriedade SECURITY \_ DESCRIPTOR.**


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

[Sobre Windows gerenciamento remoto](about-windows-remote-management.md)
</dt> <dt>

[Gerenciamento de hardware remoto](remote-hardware-management.md)
</dt> <dt>

[**Resourcelocator**](resourcelocator.md)
</dt> </dl>

 

 