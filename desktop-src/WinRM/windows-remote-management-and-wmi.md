---
title: Windows Gerenciamento Remoto e WMI
description: Windows O Gerenciamento Remoto pode ser usado para recuperar dados expostos por meio Windows Instrumentação de Gerenciamento.
ms.assetid: a625440b-a839-487d-b862-e35934f24e1f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4d4fab5cd1ee27f664fc43838a62db949c5892147818466edf649641eff203b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642466"
---
# <a name="windows-remote-management-and-wmi"></a>Windows Gerenciamento Remoto e WMI

Windows O Gerenciamento Remoto pode ser usado para recuperar dados expostos Windows Instrumentação de Gerenciamento[(WMI](/windows/desktop/WmiSdk/wmi-start-page) e [MI).](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) Você pode obter dados WMI com scripts ou aplicativos que usam a API de [Script WinRM](winrm-scripting-api.md) ou por meio da ferramenta de linha de comando **Winrm.**

O WinRM dá suporte à maioria das classes e operações WMI familiares, incluindo objetos inseridos. O WinRM pode aproveitar o WMI para coletar dados [*sobre*](windows-remote-management-glossary.md) recursos ou gerenciar recursos em um Windows operacional baseado em dados. Isso significa que você pode obter dados sobre objetos como discos, adaptadores de rede, serviços ou processos em sua empresa por meio do conjunto existente de [classes WMI](/windows/desktop/WmiSdk/wmi-classes). Você também pode acessar os dados de hardware que estão disponíveis no provedor [IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)WMI padrão .

## <a name="identifying-a-wmi-resource"></a>Identificando um recurso WMI

Você pode referenciar uma [](windows-remote-management-glossary.md) classe WMI como um recurso no WinRM e no protocolo WS-Management: um tipo de entidade gerenciada, como um serviço ou um disco.

Uma classe ou método WMI é identificado por [*um URI,*](windows-remote-management-glossary.md)assim como qualquer outro recurso é ao usar o protocolo WS-Management. O URI pode especificar um recurso WMI (classe), uma ação WMI (método) ou identificar uma instância específica de uma classe em mensagens [*enviadas*](windows-remote-management-glossary.md) por uma rede. Para obter mais informações, consulte [URIs de recurso.](resource-uris.md)

## <a name="constructing-the-uri-prefix-for-wmi-classes"></a>Construindo o prefixo de URI para classes WMI

O prefixo de URI contém uma parte fixa e o namespace WMI. Por exemplo, o prefixo de URI Windows Server que contém a parte fixa do prefixo é: `http://schemas.microsoft.com/wbem/wsman/1/wmi/<WmiNamespace>` . Isso permite que o prefixo de URI seja gerado para qualquer namespace WMI. Por exemplo, para acessar o namespace WMI padrão raiz, use o seguinte prefixo de URI: **\\** `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/default/` .

A maioria das classes WMI para gerenciamento está no namespace **\\ raiz cimv2.** Para acessar classes e instâncias no namespace **\\ raiz cimv2,** use o prefixo de URI: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` . Para obter mais informações, consulte [URIs de recurso.](resource-uris.md)

## <a name="generating-a-complete-uri-for-wmi-classes"></a>Gerando um URI completo para classes WMI

O URI que você fornece, seja para a ferramenta de linha de **comando do Winrm** ou para um script, consiste no prefixo mais a especificação do recurso.

O procedimento a seguir descreve como gerar um URI de recurso para obter uma classe WMI ou para usar em uma operação de enumeração.

**Para gerar um URI de recurso para uma classe WMI**

1.  Comece com o prefixo que indica que o WS-Management de protocolo deve ser usado.

    https://schemas.microsoft.com/wbem/wsman/1

    O prefixo de URI de recurso para classes WMI é sempre o mesmo. Para obter mais informações, consulte [Prefixos de URI](uri-prefixes.md).

2.  Adicione o namespace WMI ao prefixo.

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`

3.  Adicione o nome da classe.

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service`

4.  Para definir o valor de uma propriedade ou invocar um método específico, adicione o valor de chave ou os valores necessários para a classe .

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Name=Winmgmt`

    Se você deixar o valor da chave em branco, não alterará o valor da propriedade original.

    > [!Note]  
    > Deixar o valor da chave em branco define o valor da propriedade como **NULL.**

     

## <a name="locating-a-wmi-resource-with-winrm"></a>Localizando um recurso WMI com WinRM

Você pode obter dados WMI por meio da ferramenta de linha de comando, **Winrm** ou por meio de um script Visual Basic que usa a API de [Script WinRM](winrm-scripting-api.md). Você não usa um [caminho WMI para](/windows/desktop/WmiSdk/describing-the-location-of-a-wmi-object) localizar um recurso. Em vez disso, você converte o namespace e a hierarquia do WMI em um [*URI*](windows-remote-management-glossary.md).

O URI do WinRM para uma classe WMI contém duas partes: o [prefixo de URI](uri-prefixes.md) e a classe que você deseja acessar.

Por exemplo, o URI a seguir pode ser fornecido ao [**método Session.Enumerate**](session-enumerate.md) para listar todos os serviços em um computador. O prefixo de URI é `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` e a classe é Serviço [**Win32. \_**](/windows/desktop/CIMWin32Prov/win32-service)

`strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"`

No WMI, liste os dados de todas as instâncias de um recurso ou classe de várias maneiras:

-   Uma consulta para todas as instâncias desse recurso.

    `Set colServices = objWMIService.ExecQuery("Select * from Win32_Service")`

-   Uma chamada para [**SWbemServices.InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) ou [**SWbemObject.Instances \_**](/windows/desktop/WmiSdk/swbemobject-instances-).

    `Set colServices = InstancesOf("Win32_Service")`

No WinRM, há uma maneira de listar todas as instâncias de um recurso: [**Session.Enumerate**](session-enumerate.md).


```VB
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
Set colServices = objSession.Enumerate( strResource )
```



## <a name="locating-a-specific-instance-of-a-wmi-resource"></a>Localizando uma instância específica de um recurso WMI

No WMI, você pode designar uma instância específica de uma classe especificando valores para as propriedades da chave ou consultando uma instância que corresponde a uma lista de valores de propriedade. As propriedades de chave têm o [**qualificador de chave**](/windows/desktop/WmiSdk/key-qualifier)WMI .

Você pode obter uma instância específica de uma classe de várias maneiras:

-   Uma chamada para [**Session.Enumerate com**](session-enumerate.md) os *parâmetros de filtro* e dialeto para criar uma consulta. 

    ```VB
    RemoteComputer = "servername.domain.com"
    strDialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

    strFilter = "SELECT * FROM Win32_Share WHERE Name='Admin$'"
    Set objResultSet = objSession.Enumerate(strResource, strFilter, strDialect)
    ```

    

-   Uma chamada para [**SWbemServices.Get.**](/windows/desktop/WmiSdk/swbemservices-get) Para [**Session.Get**](session-get.md), você deve fornecer um ou mais valores de chave específicos, precedido por um ponto de interrogação (?).

    O formato do URI de uma instância específica é `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/WMI\_Class?Key1=Value` .

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

    Uma classe WMI pode ter mais de uma chave. Os pares nome-valor da chave são separados por um sinal de "+". Nesse caso, o formato é: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Key1=Value1+Key2=Value2` .

    A sintaxe winRM para obter um objeto WMI singleton é diferente da WMI. Um singleton é uma classe WMI definida para que apenas uma instância seja permitida. [**Win32 \_ CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) ou [**Win32 \_ WMISetting são**](/windows/desktop/CIMWin32Prov/win32-wmisetting) exemplos de uma classe singleton WMI.

    A sintaxe WMI para singletons é mostrada no exemplo de código VBScript a seguir.

    ```VB
    Set TimeObject = objWMIService.Get("Win32_CurrentTime=@")
    ```

    

    O exemplo a seguir mostra a sintaxe singleton do WinRM que não usa "@".

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"
    ```

    

-   Adicionar um [*seletor*](windows-remote-management-glossary.md) a [**um objeto ResourceLocator**](resourcelocator.md) [**ou IWSManResourceLocator.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)

    O exemplo de código VBScript a seguir mostra como usar um seletor para obter uma instância específica do [**Processador Win32. \_**](/windows/desktop/CIMWin32Prov/win32-processor)

    ```VB
    strUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Processor"
    Set objWsman = CreateObject("Wsman.Automation")
    Set Session = objWsman.CreateSession
    Set Locator = objWsman.CreateResourceLocator(strUri)
    Locator.AddSelector "DeviceID", "CPU0"
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre Windows gerenciamento remoto](about-windows-remote-management.md)
</dt> <dt>

[Prefixos de URI](uri-prefixes.md)
</dt> <dt>

[URIs do Recurso](resource-uris.md)
</dt> <dt>

[Scripts no Windows Gerenciamento Remoto](scripting-in-windows-remote-management.md)
</dt> </dl>
