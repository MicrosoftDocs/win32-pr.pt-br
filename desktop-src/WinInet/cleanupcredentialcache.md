---
title: Função CleanupCredentialCache
description: Implementado por determinados provedores de suporte de segurança (SSP) para liberar o cache de credenciais do SSP.
ms.assetid: e60870e6-22d3-4321-abca-a5b9d2b0ce2d
keywords:
- Função CleanupCredentialCache WinINet
topic_type:
- apiref
api_name:
- CleanupCredentialCache
api_location:
- MSNSSPC.dll
- MSAPSSPC.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53464073dd59837ba8026bbec03118055fba20cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085187"
---
# <a name="cleanupcredentialcache-function"></a>Função CleanupCredentialCache

A função **CleanupCredentialCache** é implementada por determinados provedores de suporte de segurança (SSP) para liberar o cache de credenciais do SSP.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI CleanupCredentialCache(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

**True** se a função for realizada com sucesso; caso contrário, **false**.

## <a name="remarks"></a>Comentários

A função **CleanupCredentialCache** é implementada pelos seguintes SSPs:

-   MSNSSPC.dll
-   MSAPSSPC.dll

A implementação de **CleanupCredentialCache** por esses SSPs sempre retorna **true**.

Antes de tentar obter um identificador de módulo para exportar **CleanupCredentialCache**, o aplicativo deve verificar se o SSP que foi carregado é um dos SSPs conhecidos que implementam a função **CleanupCredentialCache** .

Para liberar o cache de credenciais do SSP, o aplicativo deve obter um identificador de módulo para o SSP chamando a função [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) . Depois de obter o módulo, o aplicativo deve exportar a função **CleanupCredentialCache** implementada pelo SSP chamando a função [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) , passando o módulo retornado por **GetModuleHandle** e **CleanupCredentialCache** como parâmetros de entrada.

Como todos os outros aspectos da API do WinINet, essa função não pode ser chamada com segurança de em DllMain ou os construtores e destruidores de objetos globais.

> [!Note]  
> O WinINet não oferece suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                                 |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                       |
| DLL<br/>                      | <dl> <dt>MSNSSPC.dll; </dt> <dt>MSAPSSPC.dll</dt> </dl> |



 

