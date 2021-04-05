---
description: Quando ele instala um provedor de rede, seu aplicativo deve criar as chaves do registro e os valores descritos neste tópico.
ms.assetid: cc5a4a7b-02b5-4ecd-967c-de0656f00846
title: Chaves do registro de autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee2e42febe7516060dd61a7b751a33dcf62cb9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921949"
---
# <a name="authentication-registry-keys"></a>Chaves do registro de autenticação

Quando ele instala um provedor de rede, seu aplicativo deve criar as chaves do registro e os valores descritos neste tópico. Essas chaves e valores fornecem informações para o MPR sobre os provedores de rede instalados no sistema. O MPR verifica essas chaves quando ele inicia e carrega as DLLs do provedor de rede que ele encontra.

Antes de criar um conjunto de chaves para armazenar informações sobre seu provedor de rede, você deve adicionar o nome do seu provedor de rede à chave de **ordem** . Essa chave é uma subchave da seguinte chave:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
```

A chave **Order** contém um único valor, **ProviderOrder**, que lista os provedores instalados e especifica a ordem na qual eles devem ser testados durante as operações que alternam provedores até que um provedor de aceitação seja encontrado.

O valor **ProviderOrder** contém uma lista separada por vírgulas de nomes de chave. Cada nome de chave no **ProviderOrder** identifica um provedor de rede. Quando o MPR percorre os provedores, ele os chama na ordem em que aparecem nessa lista.

O nome do provedor definido em **ProviderOrder** também deve ser usado como o nome da chave do registro que contém informações sobre esse provedor. As chaves do registro específicas do provedor são criadas como subchaves da seguinte chave:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

Em outras palavras, os nomes de provedor especificados em **ProviderOrder** são o caminho para o registro das chaves específicas do provedor de rede, em relação ao seguinte caminho:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

Quando o serviço do provedor de rede estiver instalado, o aplicativo de instalação deverá adicionar uma chave da seguinte maneira:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            ProviderName
```

Em que *ProviderName* é o nome do provedor de rede, conforme especificado no valor **ProviderOrder** da chave **Order** . O valor do **grupo** sob a chave *ProviderName* deve ser definido como "NetworkProvider". Isso identifica o serviço como estando no grupo de provedores de rede.

Você também deve criar uma subchave de *ProviderName*, **NetworkProvider**. Essa chave contém os seguintes valores que descrevem o provedor de rede.



| Valor                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nome**<br/>         | Contém o nome do provedor. Esse nome é exibido para o usuário como o nome da rede nas caixas de diálogo de procura e deve corresponder ao campo **lpProvider** retornado nas estruturas do [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) . Esse nome deve ser uma variação do nome do produto, preferencialmente com alguma indicação da empresa também, para que seja claro e exclusivo. "MS-LanMan", por exemplo, é um bom nome, enquanto "The net" seria uma opção ruim.<br/> |
| **ProviderPath**<br/> | Contém o caminho completo da DLL que implementa o provedor de rede. O MPR chama [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) neste caminho.<br/>                                                                                                                                                                                                                                                                                                                                |



 

Os valores a seguir são usados somente por provedores de rede que dão suporte às funções de gerenciamento de credenciais, [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) e [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify).



| Valor                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Classe**<br/>               | Um **DWORD** que identifica a classe, ou tipo, da funcionalidade do provedor à qual esse provedor dá suporte. Os valores podem ser Unidos pelo operador **or** quando apropriado. Os valores válidos para isso são \_ \_ classe de rede Wn, \_ classe de credencial WN \_ , \_ \_ classe AUTHENT primária WN \_ e classe de \_ serviço WN \_ .<br/> Embora um provedor possa dar suporte à funcionalidade de autenticador primário, outro meio será usado para determinar qual autenticador é primário.<br/> **Windows XP/2000:** Não há suporte para a alternância de autenticadores primários, portanto, esse valor é ignorado. <br/> |
| **AuthentProviderPath**<br/> | Esse é o nome de arquivo totalmente qualificado para a DLL que exporta as funções de gerenciamento de credenciais. Esse valor é útil (mas não obrigatório) somente quando o provedor é identificado como sendo uma classe de CREDENCIAl \_ ou \_ provedor de classe AUTHENT primário \_ . Se esse valor não estiver presente para um provedor dessa classe, as funções de gerenciamento de credenciais deverão ser exportadas da DLL identificadas pelo valor ProviderPath. Esse valor será usado somente se for desejável empacotar as funções de rede e as funções do Gerenciador de credenciais em DLLs separadas.<br/>  |



 

Além dos valores usados para registrar provedores de rede e gerenciadores de credenciais, você pode adicionar um valor ao registro para registrar uma DLL para receber notificações de conexão. Para fazer isso, crie um \_ valor reg Expand \_ sz na seguinte chave:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
               Notifyees
```

Esse valor deve especificar o caminho para uma DLL que implementa a [API de notificação de conexão](connection-notification-api.md). O nome desse valor pode ser qualquer coisa que você desejar, desde que ele não entre em conflito com nomes de valores preexistentes.

## <a name="example"></a>Exemplo

O exemplo a seguir mostra as chaves do registro para um sistema que tem dois provedores de rede instalados: LanmanWorkStation e AnotherNetSvc. AnotherNetSvc também é um Gerenciador de credenciais. No exemplo, os nomes de chave são negrito e os nomes de valores são itálico.

**HKEY \_ \_** Ordem do controle do sistema de computador local \\  \\ **CurrentControlSet** \\ **Control** \\ **NetworkProvider** \\ 

*ProviderOrder* = "LanmanWorkStation, AnotherNetSvc"

**HKEY \_ Sistema de \_ computador local** \\  \\ **CurrentControlSet** \\ **Control** o \\ **NetworkProvider** \\ **notifica** os

*MyNotifyApp* = "c: \\ conectar \\connect.dll"

**HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **Serviços** \\ **LanmanWorkStation**\\

*Group* = "NetworkProvider"

**HKEY \_ \_Computador local** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkStation** \\ **NetworkProvider**

*Name* = "NT LanMan"*ProviderPath* = "ntlanman.dll"

*Classe* = 0x00000001 ( \_ classe de rede WN \_ )

**HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **Serviços** \\ **AnotherNetSvc**\\

*Group* = "NetworkProvider"

**HKEY \_ \_Computador local** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **AnotherNetSvc** \\ **NetworkProvider**

*Name* = "outra rede"*ProviderPath* = "c: \\ outro \\anet.dll"

*Class* = 0x00000003 ( \_ classe de \_ credencial WN de classe de rede WN \| \_ \_ )

*AuthentProviderPath* = "c: \\ outro \\anetCM.dll"

 

