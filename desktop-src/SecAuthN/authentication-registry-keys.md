---
description: Quando ele instala um provedor de rede, seu aplicativo deve criar as chaves do Registro e os valores descritos neste tópico.
ms.assetid: cc5a4a7b-02b5-4ecd-967c-de0656f00846
title: Chaves do Registro de Autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c245cdb27a0d661e7e6df82ed0d1d0ed35a59ea05bf74bf98ebd39ba3dc791
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883676"
---
# <a name="authentication-registry-keys"></a>Chaves do Registro de Autenticação

Quando ele instala um provedor de rede, seu aplicativo deve criar as chaves do Registro e os valores descritos neste tópico. Essas chaves e valores fornecem informações à MPR sobre os provedores de rede instalados no sistema. A MPR verifica essas chaves quando ela é iniciada e carrega as DLLs do provedor de rede que encontra.

Antes de criar um conjunto de chaves para manter informações sobre seu provedor de rede, você deve adicionar o nome do provedor de rede à chave **de** pedido. Essa chave é uma sub-chave da seguinte chave:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
```

A  chave de pedido contém um único valor, **ProviderOrder,** que lista os provedores instalados e especifica a ordem na qual eles devem ser tentados durante operações que passam por provedores até que um provedor de aceitação seja encontrado.

O **valor ProviderOrder** contém uma lista separada por vírgulas de nomes de chave. Cada nome de chave **em ProviderOrder** identifica um provedor de rede. Quando a MPR passa pelos provedores, ela os chama na ordem em que aparecem nessa lista.

O nome do provedor definido **em ProviderOrder** também deve ser usado como o nome da chave do Registro que contém informações sobre esse provedor. As chaves do Registro específicas do provedor são criadas como sub-chaves da seguinte chave:

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

Quando o serviço de provedor de rede estiver instalado, o aplicativo de instalação deverá adicionar uma chave da seguinte forma:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            ProviderName
```

Em *que ProviderName* é o nome do provedor de rede, conforme especificado no valor **ProviderOrder** da **chave de** ordem. O **valor** Group na chave *ProviderName* deve ser definido como "NetworkProvider". Isso identifica o serviço como sendo no grupo de provedores de rede.

Você também deve criar uma sub-chave *de ProviderName*, **networkprovider**. Essa chave contém os seguintes valores que descrevem o provedor de rede.



| Valor                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nome**<br/>         | Contém o nome do provedor. Esse nome é exibido para o usuário como o nome da rede nas caixas de diálogo procurar e deve corresponder ao campo **lpProvider** retornado em estruturas [**NETRESOURCE.**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) Esse nome deve ser uma variação do nome do produto, preferencialmente com alguma indicação da empresa também, para que ele seja claro e exclusivo. "MS-LanMan", por exemplo, é um bom nome, enquanto "The Net" seria uma opção ruim.<br/> |
| **ProviderPath**<br/> | Contém o caminho completo da DLL que implementa o provedor de rede. A MPR [**chama LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) nesse caminho.<br/>                                                                                                                                                                                                                                                                                                                                |



 

Os valores a seguir são usados apenas por provedores de rede que suportam as funções de gerenciamento de credenciais, [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) e [**NPPasswordChangeNotify.**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify)



| Valor                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Classe**<br/>               | Um **DWORD** que identifica a classe, ou o tipo, da funcionalidade do provedor compatível com esse provedor. Os valores podem ser unidos pelo **operador OR** quando apropriado. Os valores válidos para isso são \_ WN NETWORK \_ CLASS, WN \_ CREDENTIAL \_ CLASS, WN \_ PRIMARY \_ AUTHENT \_ CLASS e WN SERVICE \_ \_ CLASS.<br/> Embora um provedor possa dar suporte à funcionalidade do autenticador primário, outro meio será usado para determinar qual autenticador é primário.<br/> **Windows XP/2000:** Não há suporte para alternar autenticadores primários, portanto, esse valor é ignorado. <br/> |
| **AuthentProviderPath**<br/> | Esse é o nome de arquivo totalmente qualificado para a DLL que exporta as Funções de Gerenciamento de Credenciais. Esse valor é útil (mas não obrigatório) somente quando o provedor é identificado como sendo um provedor CREDENTIAL CLASS ou \_ PRIMARY \_ AUTHENT \_ CLASS. Se esse valor não estiver presente para um provedor dessa classe, as funções de gerenciamento de credenciais deverão ser exportadas da DLL identificada pelo valor ProviderPath. Esse valor será usado somente se for desejável empacotar as funções de rede e as funções do gerenciador de credenciais em DLLs separadas.<br/>  |



 

Além dos valores usados para registrar provedores de rede e gerenciadores de credenciais, você pode adicionar um valor ao Registro para registrar uma DLL para receber notificações de conexão. Para fazer isso, crie um valor REG \_ EXPAND \_ SZ na seguinte chave:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
               Notifyees
```

Esse valor deve especificar o caminho para uma DLL que implementa a [conexão API de Notificação](connection-notification-api.md). O nome desse valor pode ser qualquer coisa que você quiser, desde que ele não entre em conflito com nomes de valor preexistência.

## <a name="example"></a>Exemplo

O exemplo a seguir mostra as chaves do Registro para um sistema que tem dois provedores de rede instalados: LanmanWorkStation e AnotherNetSvc. AnotherNetSvc também é um gerenciador de credenciais. No exemplo, os nomes de chave são negrito e os nomes de valor são itálico.

**HKEY \_ Local \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Control** \\ **NetworkProvider** \\ **order**

*ProviderOrder* = "LanmanWorkStation,AnotherNetSvc"

**HKEY \_ Rede \_ de controle Local MACHINE** \\ **SYSTEM** \\ **CurrentControlSetProvider** \\  \\  \\ **Notifyees**

*MyNotifyApp* = "c: \\ connect \\connect.dll"

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkStation**\\

*Grupo* = "NetworkProvider"

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkStation** \\ **NetworkProvider**

*Name* = "NT LanMan"*ProviderPath* = "ntlanman.dll"

*Classe* = 0x00000001 (WN \_ NETWORK \_ CLASS)

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **AnotherNetSvc**\\

*Grupo* = "NetworkProvider"

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **AnotherNetSvc** \\ **NetworkProvider**

*Name* = "Another Network"*ProviderPath* = "c: \\ another \\anet.dll"

*Classe* = 0x00000003 (CLASSE \_ WN NETWORK \_ \| WN \_ CREDENTIAL \_ CLASS)

*AuthentProviderPath* = "c: \\ outro \\anetCM.dll"

 

