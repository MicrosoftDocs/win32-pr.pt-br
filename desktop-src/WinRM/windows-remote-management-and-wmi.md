---
title: Gerenciamento Remoto do Windows e WMI
description: Gerenciamento Remoto do Windows pode ser usado para recuperar dados expostos por Instrumentação de Gerenciamento do Windows.
ms.assetid: a625440b-a839-487d-b862-e35934f24e1f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6942e89ea2e63ef809f3452e6ce55a493662c938
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "105763986"
---
# <a name="windows-remote-management-and-wmi"></a>Gerenciamento Remoto do Windows e WMI

Gerenciamento Remoto do Windows pode ser usado para recuperar dados expostos por Instrumentação de Gerenciamento do Windows ([WMI](/windows/desktop/WmiSdk/wmi-start-page) e [mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)). Você pode obter dados do WMI com scripts ou aplicativos que usam a [API de script do WinRM](winrm-scripting-api.md) ou por meio da ferramenta de linha de comando **WinRM** .

O WinRM oferece suporte à maioria das classes e operações WMI familiares, incluindo objetos incorporados. O WinRM pode aproveitar o WMI para coletar dados sobre [*recursos*](windows-remote-management-glossary.md) ou para gerenciar recursos em um sistema operacional baseado no Windows. Isso significa que você pode obter dados sobre objetos como discos, adaptadores de rede, serviços ou processos em sua empresa por meio do conjunto existente de [classes WMI](/windows/desktop/WmiSdk/wmi-classes). Você também pode acessar os dados de hardware que estão disponíveis no provedor padrão de [IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)do WMI.

## <a name="identifying-a-wmi-resource"></a>Identificando um recurso WMI

Você pode fazer referência a uma classe WMI como um [*recurso*](windows-remote-management-glossary.md) no WinRM e no protocolo WS-Management: um tipo de entidade gerenciada, como um serviço ou um disco.

Uma classe ou um método WMI é identificado por um [*URI*](windows-remote-management-glossary.md), assim como qualquer outro recurso é ao usar o protocolo WS-Management. O URI pode especificar um recurso de WMI (classe), uma ação de WMI (método) ou identificar uma instância específica de uma classe em [*mensagens*](windows-remote-management-glossary.md) enviadas por uma rede. Para obter mais informações, consulte [URIs de recurso](resource-uris.md).

## <a name="constructing-the-uri-prefix-for-wmi-classes"></a>Construindo o prefixo URI para classes WMI

O prefixo URI contém uma parte fixa e o namespace WMI. Por exemplo, o prefixo URI no Windows Server que contém a parte fixa do prefixo é: `http://schemas.microsoft.com/wbem/wsman/1/wmi/<WmiNamespace>` . Isso permite que o prefixo de URI seja gerado para qualquer namespace WMI. Por exemplo, para acessar o namespace WMI **\\ padrão raiz** , use o seguinte prefixo de URI: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/default/` .

A maioria das classes WMI para gerenciamento está no namespace **raiz \\ cimv2** . Para acessar classes e instâncias no namespace **raiz \\ cimv2** , use o prefixo URI: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` . Para obter mais informações, consulte [URIs de recurso](resource-uris.md).

## <a name="generating-a-complete-uri-for-wmi-classes"></a>Gerando um URI completo para classes WMI

O URI que você fornece, seja para a ferramenta de linha de comando **WinRM** ou para um script, consiste no prefixo mais a especificação de recurso.

O procedimento a seguir descreve como gerar um URI de recurso para obter uma classe WMI ou para usar em uma operação enumerar.

**Para gerar um URI de recurso para uma classe WMI**

1.  Comece com o prefixo que indica que o esquema de protocolo de WS-Management deve ser usado.

    https://schemas.microsoft.com/wbem/wsman/1

    O prefixo do URI de recurso para classes WMI é sempre o mesmo. Para obter mais informações, consulte [prefixos de URI](uri-prefixes.md).

2.  Adicione o namespace WMI ao prefixo.

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`

3.  Adicione o nome da classe.

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service`

4.  Para definir o valor de uma propriedade ou para invocar um método específico, adicione o valor de chave ou os valores necessários para a classe.

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Name=Winmgmt`

    Se você deixar o valor da chave em branco, não será alterado o valor da propriedade original.

    > [!Note]  
    > Deixar o valor da chave em branco define o valor da propriedade como **NULL**.

     

## <a name="locating-a-wmi-resource-with-winrm"></a>Localizando um recurso WMI com o WinRM

Você pode obter dados WMI por meio da ferramenta de linha de comando, **WinRM** ou por meio de um script de Visual Basic que usa a [API de script do WinRM](winrm-scripting-api.md). Você não usa um [caminho WMI](/windows/desktop/WmiSdk/describing-the-location-of-a-wmi-object) para localizar um recurso. Em vez disso, você converte o namespace e a hierarquia do WMI em um [*URI*](windows-remote-management-glossary.md).

O URI do WinRM para uma classe WMI contém duas partes: o [prefixo do URI](uri-prefixes.md) e a classe que você deseja acessar.

Por exemplo, o URI a seguir pode ser fornecido para o método [**Session. Enumerate**](session-enumerate.md) para listar todos os serviços em um computador. O prefixo do URI é `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` , e a classe é o [**\_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service).

`strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"`

No WMI, liste os dados de todas as instâncias de um recurso ou classe de várias maneiras:

-   Uma consulta para todas as instâncias desse recurso.

    `Set colServices = objWMIService.ExecQuery("Select * from Win32_Service")`

-   Uma chamada para [**SWbemServices. InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) ou [**SWbemObject. Instances \_**](/windows/desktop/WmiSdk/swbemobject-instances-).

    `Set colServices = InstancesOf("Win32_Service")`

No WinRM, há uma maneira de listar todas as instâncias de um recurso: [**Session. Enumerate**](session-enumerate.md).


```VB
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
Set colServices = objSession.Enumerate( strResource )
```



## <a name="locating-a-specific-instance-of-a-wmi-resource"></a>Localizando uma instância específica de um recurso WMI

No WMI, você pode designar uma instância específica de uma classe especificando valores para as propriedades de chave ou consultando uma instância que corresponda a uma lista de valores de propriedade. As propriedades de chave têm o [**qualificador de chave**](/windows/desktop/WmiSdk/key-qualifier)WMI.

Você pode obter uma instância específica de uma classe de várias maneiras:

-   Uma chamada para [**Session. enumerar**](session-enumerate.md) com os parâmetros *Filter* e *Dialect* para criar uma consulta.

    ```VB
    RemoteComputer = "servername.domain.com"
    strDialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

    strFilter = "SELECT * FROM Win32_Share WHERE Name='Admin$'"
    Set objResultSet = objSession.Enumerate(strResource, strFilter, strDialect)
    ```

    

-   Uma chamada para [**SWbemServices. Get**](/windows/desktop/WmiSdk/swbemservices-get). Para [**Session. Get**](session-get.md), você deve fornecer um ou mais valores de chave específicos, precedidos por um ponto de interrogação (?).

    O formato do URI para uma instância específica é `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/WMI\_Class?Key1=Value` .

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

    Uma classe WMI pode ter mais de uma chave. Os pares nome-valor da chave são separados por um sinal "+". Nesse caso, o formato é: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Key1=Value1+Key2=Value2` .

    A sintaxe do WinRM para obter um objeto WMI singleton é diferente do WMI. Um singleton é uma classe WMI definida para que apenas uma instância seja permitida. [**Win32 \_**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) Os [**\_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) atuais ou Win32 são exemplos de uma classe singleton WMI.

    A sintaxe de WMI para singletons é mostrada no exemplo de código VBScript a seguir.

    ```VB
    Set TimeObject = objWMIService.Get("Win32_CurrentTime=@")
    ```

    

    O exemplo a seguir mostra a sintaxe de singleton do WinRM que não usa "@".

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"
    ```

    

-   Adicionando um [*seletor*](windows-remote-management-glossary.md) a um objeto [**ResourceLocator**](resourcelocator.md) ou [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) .

    O exemplo de código VBScript a seguir mostra como usar um seletor para obter uma instância específica do [**\_ processador Win32**](/windows/desktop/CIMWin32Prov/win32-processor).

    ```VB
    strUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Processor"
    Set objWsman = CreateObject("Wsman.Automation")
    Set Session = objWsman.CreateSession
    Set Locator = objWsman.CreateResourceLocator(strUri)
    Locator.AddSelector "DeviceID", "CPU0"
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre Gerenciamento Remoto do Windows](about-windows-remote-management.md)
</dt> <dt>

[Prefixos de URI](uri-prefixes.md)
</dt> <dt>

[URIs do Recurso](resource-uris.md)
</dt> <dt>

[Criando scripts no Gerenciamento Remoto do Windows](scripting-in-windows-remote-management.md)
</dt> </dl>
