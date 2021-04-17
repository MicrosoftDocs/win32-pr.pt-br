---
description: Ocasionalmente, talvez você queira atualizar apenas parte de uma instância do.
ms.assetid: c92bf8f9-9cac-4cf0-a45d-f60aee5a9ec2
ms.tgt_platform: multiple
title: Atualizando parte de uma instância
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eaf58bfc151358a2b4f282815769d1b19c068f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782645"
---
# <a name="updating-part-of-an-instance"></a>Atualizando parte de uma instância

Ocasionalmente, talvez você queira atualizar apenas parte de uma instância do. Por exemplo, algumas instâncias têm um grande número de propriedades. Se você precisava atualizar um grande número dessas instâncias, poderá reduzir o desempenho do sistema. Portanto, você pode optar por atualizar apenas parte da instância e, assim, reduzir a quantidade de informações que você deve enviar e recuperar de e para o WMI. No entanto, o WMI não oferece suporte diretamente a operações de instância parcial nem a maioria dos provedores. Portanto, se você escrever um aplicativo que usa operações de instância parcial, esteja preparado para que suas chamadas falhem com o **\_ provedor WBEM \_ e \_ não \_ compatível** ou o código de erro **WBEM \_ e \_ sem \_ suporte** em C++. Em linguagens de script, os códigos de erro são **wbemErrProviderNotCapable** ou **wbemErrNotSupported**.

No script, essa operação só é necessária para ajudar no desempenho ao atualizar uma ou duas propriedades graváveis em um número muito grande de objetos em uma empresa. Caso contrário, as chamadas normais do VBScript para [**SWbemObject \_ . put**](swbemobject-put-.md) ou [**SWbemObject \_ . PutAsync**](swbemobject-putasync-.md), embora pareçam gravar o objeto inteiro, estão, na verdade, atualizando apenas as propriedades que o provedor tem habilitado para gravação.

O procedimento a seguir descreve como solicitar uma atualização de instância parcial usando o PowerShell.

**Para solicitar uma atualização de instância parcial usando o PowerShell**

1.  Recupere o caminho do objeto que você deseja atualizar.

    Você pode descrever o caminho manualmente ou, caso contrário, consultar o objeto e, em seguida, recuperar a propriedade **\_ \_ Path** .

    ```PowerShell
    $myWMIDrivePath = (get-wmiObject Win32_LogicalDisk -filter "Name = 'C:'").__Path
    #or
    $myWmiDrivePath = \\myComputer\root\cimv2:Win32_LogicalDisk.DeviceID="C:"
    ```

    

2.  Configure uma tabela de hash listando os nomes das propriedades a serem atualizadas e use essa tabela de hash em uma chamada para [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).

    ```PowerShell
    $newDriveName = @{VolumeName = "OSDisk"}
    Set-WmiInstance -Path $myWMIDrivePath -Arguments $newDriveName
    ```

    

O procedimento a seguir descreve como solicitar uma atualização de instância parcial usando C#.

> [!Note]  
> **System. Management** foi o namespace .net original usado para acessar o WMI; no entanto, as APIs nesse namespace geralmente são mais lentas e não são dimensionadas em relação às suas contrapartes mais modernas de **Microsoft. Management. Infrastructure** .

 

**Para solicitar uma atualização de instância parcial usando C #**

1.  Crie um novo objeto [ManagementObject](/dotnet/api/system.management.managementobject) que representa a instância específica a ser atualizada.

    ```PowerShell
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

2.  Defina o valor da propriedade com uma chamada para [ManagementObject. SetPropertyValue](/dotnet/api/system.management.managementbaseobject.setpropertyvalue#System_Management_ManagementBaseObject_SetPropertyValue_System_String_System_Object_).

    ```CSharp
    myDisk.SetPropertyValue("VolumeName", "OSDisk");
    ```

    

O procedimento a seguir descreve como solicitar uma atualização de instância parcial usando o VBScript.

**Para solicitar uma atualização de instância parcial usando o VBScript**

1.  Crie um objeto de contexto [**SWbemNamedValueSet**](swbemnamedvalueset.md) .

    ```VB
    Set objwbemNamedValueSet = CreateObject ("WbemScripting.SWbemNamedValueSet")
    ```

    

2.  Adicione os valores de extensão Put " \_ \_ colocar \_ extensões" e " \_ \_ colocar a solicitação de \_ \_ cliente ext" no objeto de \_ contexto usando o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) .

    ```VB
    objwbemNamedValueSet.Add "__PUT_EXTENSIONS", True
    objwbemNamedValueSet.Add "__PUT_EXT_CLIENT_REQUEST", True
    ```

    

3.  Configure uma matriz que liste os nomes das propriedades a serem atualizadas e adicione essa matriz ao objeto de contexto [**SWbemNamedValueSet**](swbemnamedvalueset.md) com o valor de extensão Put " \_ \_ Put \_ ext \_ Properties".

    ```VB
    arProperties = Array("propertyname1", "propertyname2") 
    objwbemNamedValueSet.Add "__PUT_EXT_PROPERTIES", arProperties
    ```

    

4.  Defina o parâmetro *iFlags* da chamada [**SWbemObject. put \_**](swbemobject-put-.md) para **wbemChangeFlagUpdateOnly**. Sem esse sinalizador, a chamada falhará com um contexto inválido.

5.  Passe o sinalizador e o objeto de contexto para o provedor no parâmetro *objwbemNamedValueSet* de [**SWbemObject. put \_**](swbemobject-put-.md) ou [**SWbemObject. PutAsync \_**](swbemobject-putasync-.md).

    ```VB
    call objSystem.put_( wbemChangeFlagUpdateOnly, objwbemNamedValueSet)
    ```

    

O procedimento a seguir descreve como solicitar uma atualização de instância parcial usando C++.

**Para solicitar uma atualização de instância parcial usando C++**

1.  Crie um objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) com uma chamada para [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    Um objeto de contexto é um objeto que o WMI usa para passar mais informações para um provedor WMI. Nesse caso, você está usando o objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) para instruir o provedor a aceitar atualizações de instância parcial.

2.  Adicione os \_ \_ \_ valores nomeados "colocar extensões" e " \_ \_ colocar a solicitação de \_ \_ cliente ext \_ " ao objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) com uma chamada para [**IWbemContext:: SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).

    A tabela a seguir lista o significado de " \_ \_ colocar \_ extensões" e " \_ \_ colocar a solicitação do \_ \_ cliente ext \_ ".

    

    | Valor nomeado                     | Descrição                                                                                                                                                                                                                                             |
    |---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | " \_ \_ colocar \_ extensões"           | **VT \_ BOOL** definido como **Variant \_ true**. Um valor que indica que um ou mais dos outros valores de contexto foram especificados. Isso permite uma verificação rápida do objeto de contexto dentro do provedor para determinar se atualizações de instância parcial estão sendo usadas. |
    | " \_ \_ colocar \_ solicitação do cliente ext. \_ \_ " | **VT \_ BOOL** definido como **Variant \_ true**. Definido pelo cliente durante a solicitação inicial. Esse valor é usado para evitar erros de reentrância.                                                                                                                   |

    

     

3.  Adicione as \_ \_ \_ Propriedades Put ext \_ estrito \_ , \_ \_ Put \_ ext \_ ou coloque o \_ \_ \_ Atomic ext \_ em qualquer combinação conforme necessário para o objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) com outra chamada para [**IWbemContext:: SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).

    A tabela a seguir lista o significado dos valores nomeados.

    

    | Valor nomeado                   | Descrição                                                                                                                                                                                                                                   |
    |-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | " \_ \_ colocar \_ \_ nulos estritos estendidos \_ " | **VT \_ BOOL** definido como **Variant \_ true**. Indica que o cliente definiu intencionalmente as propriedades para **VT \_ NULL** e espera que a operação de gravação tenha sucesso. Se o provedor não puder definir os valores como **NULL**, um erro deverá ser relatado. |
    | " \_ \_ colocar \_ Propriedades ext. \_ "    | [**SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray) de cadeias de caracteres que contém uma lista de nomes de propriedade a serem atualizados. Pode ser usado sozinho ou em combinação com " \_ \_ Put \_ ext \_ Properties". Os valores estão na instância que está sendo gravada.                           |
    | " \_ \_ colocar \_ \_ Atomic ext"        | **VT \_ BOOL** definido como **Variant \_ true**. Indica que todas as atualizações devem ter sucesso simultaneamente (semântica atômica) ou o provedor deve reverter de volta. Não pode haver nenhum sucesso parcial. Pode ser usado sozinha ou em combinação com outros sinalizadores.     |

    

     

4.  Defina o parâmetro *iFlags* como **\_ \_ \_ somente atualização do sinalizador WBEM**. Sem esse sinalizador, a chamada falhará com um contexto inválido.
5.  Passe o objeto de contexto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) em qualquer chamada [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) ou [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) no parâmetro *pCtx* .

    Passar o objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) instrui o provedor para permitir atualizações parciais de instância. Em uma atualização de instância completa, você definiria *pCtx* como **nulo**.

    O provedor poderá gravar todas as propriedades necessárias se o objeto de contexto presente na chamada não contiver " \_ \_ Put \_ Extensions". Se " \_ \_ colocar \_ extensões" estiver presente no objeto de contexto, o WMI exigirá que o provedor obedeça a semântica da operação exatamente ou, caso contrário, falha na chamada. Para obter mais informações, consulte [manipulando mensagens de acesso negado em um provedor](impersonating-a-client.md).

 

 
