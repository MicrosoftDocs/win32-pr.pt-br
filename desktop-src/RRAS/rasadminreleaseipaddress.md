---
title: Função de retorno de chamada RasAdminReleaseIpAddress
description: A função RasAdminReleaseIpAddress é uma função definida pelo aplicativo que é exportada por uma DLL de administração de servidor RAS de terceiros.
ms.assetid: 86fd9173-f158-4de5-8166-483a652a52cc
keywords:
- RasAdminReleaseIpAddress função de retorno de chamada RAS
topic_type:
- apiref
api_name:
- RasAdminReleaseIpAddress
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 102c9af7a8e38ccbbb4a7e67b2734588857ddca93da862be211fd1223133f80d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788858"
---
# <a name="rasadminreleaseipaddress-callback-function"></a>Função de retorno de chamada RasAdminReleaseIpAddress

\[A **função RasAdminReleaseIpAddress** está disponível para uso no Windows NT 4.0 e não está disponível nas versões subsequentes. Em vez disso, [**use MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress).\]

A **função RasAdminReleaseIpAddress** é uma função definida pelo aplicativo que é exportada por uma DLL de administração de servidor RAS de terceiros. RAS chama essa função para notificar a DLL de que o cliente remoto foi desconectado e que o endereço IP deve ser liberado.

## <a name="syntax"></a>Sintaxe


```C++
void CALLBACK RasAdminReleaseIpAddress(
  _In_ WCHAR  *lpszUserName,
  _In_ WCHAR  *lpszPortName,
  _In_ IPADDR *pipAddress
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszUserName* \[ Em\]
</dt> <dd>

Especifica o ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome de um usuário remoto para o qual um endereço IP foi obtido anteriormente usando a [**função RasAdminGetIpAddressForUser.**](rasadmingetipaddressforuser.md)

</dd> <dt>

*lpszPortName* \[ Em\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome da porta na qual o usuário especificado por *lpszUserName* está conectado.

</dd> <dt>

*pipAddress* \[ Em\]
</dt> <dd>

Ponteiro para uma **variável IPADDR** que especifica o endereço IP retornado para esse usuário em uma chamada anterior para [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Não há informações de erro estendidas para essa função; não chame [**GetLastError.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Comentários

O servidor RAS chama a **função RasAdminReleaseIpAddress** somente se o aplicativo retornou **TRUE** no parâmetro *bNotifyRelease* durante a chamada anterior para [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) para o usuário especificado pelo *parâmetro lpszUserName.*

O programa de instalação para uma DLL de administração RAS de terceiros deve registrar a DLL com RAS fornecendo informações sob a seguinte chave no Registro:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

Para registrar a DLL, deverão ser definidos os valores a seguir nessa chave.



| Nome do valor    | Dados do valor                                                                    |
|---------------|-------------------------------------------------------------------------------|
| *DisplayName* | Uma **cadeia \_ de caracteres REG SZ** que contém o nome de exibição amigável da DLL. |
| *DLLPath*     | Uma **cadeia \_ de caracteres REG SZ** que contém o caminho completo da DLL.                  |



 

Por exemplo, a entrada do Registro para uma DLL de administração ras de uma empresa fictícia chamada ProElectron, Inc. pode ser:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName:* **REG \_ SZ:** *DLLPath* de DLL de Administrador do Ras ProElectron: **REG \_ SZ:** C: \\ nt \\ system32 \\ntwkadm.dll

O programa de instalação para uma DLL de administração ras também deve fornecer a funcionalidade remover/desinstalar. Se um usuário remover a DLL, o programa de instalação deverá excluir as entradas do Registro da DLL.

 

 