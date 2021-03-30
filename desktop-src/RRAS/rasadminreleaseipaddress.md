---
title: Função de retorno de chamada RasAdminReleaseIpAddress
description: A função RasAdminReleaseIpAddress é uma função definida pelo aplicativo que é exportada por uma DLL de administração de servidor RAS de terceiros.
ms.assetid: 86fd9173-f158-4de5-8166-483a652a52cc
keywords:
- Função de retorno de chamada RasAdminReleaseIpAddress RAS
topic_type:
- apiref
api_name:
- RasAdminReleaseIpAddress
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d58c162ebc6d340b9bd913407bc00aac87e208e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641728"
---
# <a name="rasadminreleaseipaddress-callback-function"></a>Função de retorno de chamada RasAdminReleaseIpAddress

\[A função **RasAdminReleaseIpAddress** está disponível para uso no Windows NT 4,0 e não está disponível nas versões subsequentes. Em vez disso, use [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress).\]

A função **RasAdminReleaseIpAddress** é uma função definida pelo aplicativo que é exportada por uma DLL de administração de servidor RAS de terceiros. O RAS chama essa função para notificar a DLL de que o cliente remoto foi desconectado e que o endereço IP deve ser liberado.

## <a name="syntax"></a>Sintaxe


```C++
void CALLBACK RasAdminReleaseIpAddress(
  _In_ WCHAR  *lpszUserName,
  _In_ WCHAR  *lpszPortName,
  _In_ IPADDR *pipAddress
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszUserName* \[ no\]
</dt> <dd>

Especifica o ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome de um usuário remoto para o qual um endereço IP foi obtido anteriormente usando a função [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) .

</dd> <dt>

*lpszPortName* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome da porta na qual o usuário especificado pelo *lpszUserName* está conectado.

</dd> <dt>

*pipAddress* \[ no\]
</dt> <dd>

Ponteiro para uma variável **IPADDR** que especifica o endereço IP retornado para esse usuário em uma chamada anterior para [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Não há informações de erro estendidas para esta função; Não chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

O servidor RAS chamará a função **RasAdminReleaseIpAddress** somente se o aplicativo retornar **true** no parâmetro *bNotifyRelease* durante a chamada anterior a [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) para o usuário especificado pelo parâmetro *lpszUserName* .

O programa de instalação para uma DLL de administração de RAS de terceiros deve registrar a DLL com o RAS, fornecendo informações sob a seguinte chave no registro:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

Para registrar a DLL, defina os valores a seguir nessa chave.



| Nome do valor    | Dados do valor                                                                    |
|---------------|-------------------------------------------------------------------------------|
| *DisplayName* | Uma cadeia de caracteres **reg \_ sz** que contém o nome de exibição amigável da dll. |
| *DLLPath*     | Uma cadeia de caracteres **reg \_ sz** que contém o caminho completo da dll.                  |



 

Por exemplo, a entrada de registro para uma DLL de administração de RAS de uma empresa fictícia chamada proeletromagnéticon, Inc. pode ser:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName*: **reg \_ sz** : dll de administração de Ras proeletromagnéticos *DLLPath*: **reg \_ sz** : C: \\ NT \\ System32 \\ntwkadm.dll

O programa de instalação para uma DLL de administração de RAS também deve fornecer a funcionalidade de remoção/desinstalação. Se um usuário remover a DLL, o programa de instalação deverá excluir as entradas do registro da DLL.

 

 