---
title: Método ReleaseTargetLock ITsSbResourcePluginStoreEx
description: Libera um bloqueio em um destino.
ms.assetid: ab2ae9f3-2d38-4b31-9889-58297c574bd4
ms.tgt_platform: multiple
keywords:
- Método ReleaseTargetLock Serviços de Área de Trabalho Remota
- O método ReleaseTargetLock Serviços de Área de Trabalho Remota interface , ITsSbResourcePluginStoreEx
- Interface ITsSbResourcePluginStoreEx Serviços de Área de Trabalho Remota , método ReleaseTargetLock
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx.ReleaseTargetLock
api_location:
- SbTsV.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7fbe40d0fc7a28697d0e2fa9727f9e844eb39759db0dddf02c1d9e01bd843c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989906"
---
# <a name="itssbresourcepluginstoreexreleasetargetlock-method"></a>Método ITsSbResourcePluginStoreEx::ReleaseTargetLock

Libera um bloqueio em um destino.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReleaseTargetLock(
  [in] IUnknown *pContext
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pContext* \[ Em\]
</dt> <dd>

Um ponteiro para o contexto retornado pelo [**método AcquireTargetLock.**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Esse método só está disponível no Windows Server 2012 R2 com [KB3091411 instalado](https://support.microsoft.com/kb/3091411) na interface [**ITsSbResourcePluginStoreEx.**](itssbresourcepluginstoreex.md) Esse método está disponível na interface [**ITsSbResourcePluginStore,**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) começando com Windows Server 2016.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                             |
| Fim do suporte ao servidor<br/>    | Windows Server 2012 R2<br/>                                                             |
| Idl<br/>                      | <dl> <dt>SbTsV.idl</dt> </dl>          |
| IID<br/>                      | \_ITSSbResourcePluginStoreEx IID é definido como 80b83ffd-625d-11e5-bea1-a0481c7e9064<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md)
</dt> </dl>

 

 





