---
title: Chave AppID
description: Agrupa as opções de configuração para um ou mais objetos DCOM em um local centralizado no registro. Os objetos DCOM hospedados pelo mesmo executável são agrupados em uma AppID para simplificar o gerenciamento de configurações comuns de segurança e configuração.
ms.assetid: 4e3d8c87-e6d7-4b4d-8f72-7180be1e51cf
keywords:
- COM chave do registro AppID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b283a9cc47907cf418c2d7d6d613d151c7e5c5e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366783"
---
# <a name="appid-key"></a>Chave AppID

Agrupa as opções de configuração para um ou mais objetos DCOM em um local centralizado no registro. Os objetos DCOM hospedados pelo mesmo executável são agrupados em uma AppID para simplificar o gerenciamento de configurações comuns de segurança e configuração.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_Classe de software do computador local \\ \\ \\ AppID** \\ *{* AppID \_ GUID *}*



| Valor do Registro                                           | Descrição                                                                                                                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccessPermission**](accesspermission.md)             | Descreve a ACL (lista de controle de acesso) das entidades de segurança que podem acessar instâncias dessa classe. Essa ACL é usada somente por aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). |
| [**ActivateAtStorage**](activateatstorage.md)           | Configura o cliente para instanciar objetos no mesmo computador que o estado persistente que estão usando ou dos quais eles são inicializados.                                                                    |
| [**AppID**](appid.md)                                   | Identifica o GUID AppID que corresponde ao executável nomeado.                                                                                                                                             |
| [**AppIDFlags**](appidflags.md)                         | Configura como um servidor COM configurado para ser executado como "usuário interativo" será iniciado ou vinculado a por um cliente em uma área de trabalho não padrão.                                                              |
| [**AuthenticationLevel**](authenticationlevel.md)       | Define o nível de autenticação para aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou para aplicativos que chamam **CoInitializeSecurity** e especificam uma AppID.               |
| [**DllSurrogate**](dllsurrogate.md)                     | Permite que os servidores DLL sejam executados em um processo substituto. Se uma cadeia de caracteres vazia for especificada, o substituto fornecido pelo sistema será usado; caso contrário, o valor especifica o caminho do substituto a ser usado.                 |
| [**DllSurrogateExecutable**](dllsurrogateexecutable.md) | Permite que os servidores DLL sejam executados em um processo substituto personalizado, em conjunto com o valor do registro [**DllSurrogate**](dllsurrogate.md) .                                                                          |
| [**Pontos de extremidade**](endpoints.md)                           | Configura um aplicativo COM para usar um número de porta TCP especificado para comunicações DCOM.                                                                                                                        |
| [**LaunchPermission**](launchpermission.md)             | Descreve a lista de controle de acesso (ACL) das entidades de segurança que podem iniciar novos servidores para essa classe.                                                                                                            |
| [**LoadUserSettings**](loadusersettings.md)             | Determina se o COM carregará o perfil do usuário para servidores COM em execução como a identidade do aplicativo de usuário de inicialização.                                                                                           |
| [**LocalService**](localservice.md)                     | Instala um objeto como um aplicativo de serviço.                                                                                                                                                                    |
| [**PreferredServerBitness**](preferredserverbitness.md) | Define a arquitetura preferida, 32 bits ou 64 bits, para esse servidor COM.                                                                                                                                         |
| [**RemoteServerName**](remoteservername.md)             | Configura o cliente para solicitar que o objeto seja executado em um determinado computador sempre que uma função de ativação é chamada para a qual uma estrutura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) não é especificada.              |
| [**ROTFlags**](rotflags.md)                             | Controla o registro de um servidor COM na corrompidos (tabela de objetos em execução).                                                                                                                                    |
| [**RunAs**](runas.md)                                   | Configura uma classe para ser executada em uma conta de usuário específica quando ativada por um cliente remoto sem ser escrita como um aplicativo de serviço.                                                                       |
| [**Serviceparameters**](serviceparameters.md)           | Especifica os parâmetros de linha de comando a serem passados para um objeto instalado para uso pelo COM por meio do valor do registro [**LocalService**](localservice.md) .                                                       |
| [**SRPTrustLevel**](srptrustlevel.md)                   | Define o nível de confiança da política de restrição de software (SRP) para aplicativos.                                                                                                                                        |



 

## <a name="remarks"></a>Comentários

AppIDs são mapeados para executáveis e classes usando dois mecanismos diferentes:

-   Usando um GUID (identificador global exclusivo) de 128 bits que identifica a chave **AppID** . Uma classe indica seu AppID correspondente sob a chave [**CLSID**](clsid-key-hklm.md) em um valor nomeado "AppID". Esse mapeamento é usado durante a ativação.
-   Usando um valor nomeado que indica um nome de executável (como "MYOLDAPP.EXE"). Esse valor nomeado é do tipo **reg \_ sz** e contém a representação de cadeia de caracteres do AppID associado ao executável. Esse mapeamento é usado para obter as permissões de acesso e o nível de autenticação padrão.

A chave **HKEY \_ local \_ Machine \\ software \\ classes** corresponde à chave de **\_ \_ raiz de classes hKey** , que foi retida para compatibilidade com versões anteriores do com.

Para servidores COM, o mapeamento é geralmente gerado e gravado no registro durante o processo de registro ou durante a execução de dcomcnfg.exe. No entanto, os clientes COM que desejam definir a segurança usando a chave **AppID** devem criar chaves de registro apropriadas e especificar o mapeamento necessário chamando as [funções de registro](/windows/desktop/SysInfo/registry-functions) ou usando Regedit.exe. Os valores, como [**AccessPermission**](accesspermission.md) ou [**AuthenticationLevel**](authenticationlevel.md) , podem ser definidos para o cliente. Por exemplo, suponha que o nome do seu executável para o processo do cliente seja "YourClient.exe" e você queira definir o nível de autenticação como "nenhum". Você usaria Guidgen.exe ou Uuidgen.exe para criar o GUID que é o AppID do seu executável. Em seguida, você definiria valores no registro, conforme mostrado no exemplo a seguir, em que 00000001 representa um nível de autenticação de "nenhum":

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {MyGuid}
      AuthenticationLevel = 00000001
   MyClient.exe
      AppID = {MyGUID}
```

 

 