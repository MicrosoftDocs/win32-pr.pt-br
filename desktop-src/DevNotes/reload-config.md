---
description: Recarrega uma configuração do IME do Registro HKCU, somente no IME do japonês.
ms.assetid: 171c31ad-c925-4e18-b458-d9abf52dae9a
title: função reload_config
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- reload_config
api_type:
- DllExport
api_location:
- Imejpknl.dll
- Imejp98k.dll
ms.openlocfilehash: 343003156c2f93788ac87004657a21d3e9b31a47ff4585374836488642de3240
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571616"
---
# <a name="reload_config-function"></a>recarregar \_ função de configuração

Recarrega uma configuração do IME do Registro HKCU, somente no IME do japonês.

## <a name="syntax"></a>Sintaxe


```C++
BOOL reload_config(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Essa função retornará **true** se tiver sucesso; caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

Se nenhum valor de registro estiver presente em HKCU, a função **recarregar \_ config** gravará os dados iniciais no registro.

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imejpknl.dll; </dt> <dt>Imejp98k.dll</dt> </dl> |



 

 
