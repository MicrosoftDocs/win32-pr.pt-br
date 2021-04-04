---
title: Método ITsSbResourcePluginStoreEx ReleaseTargetLock
description: Libera um bloqueio em um destino.
ms.assetid: ab2ae9f3-2d38-4b31-9889-58297c574bd4
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ReleaseTargetLock
- Método ReleaseTargetLock Serviços de Área de Trabalho Remota, interface ITsSbResourcePluginStoreEx
- Serviços de Área de Trabalho Remota de interface ITsSbResourcePluginStoreEx, método ReleaseTargetLock
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
ms.openlocfilehash: 8fbc34bdb27e40316ea1271bf0faa5d8c6b0abfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085762"
---
# <a name="itssbresourcepluginstoreexreleasetargetlock-method"></a>Método ITsSbResourcePluginStoreEx:: ReleaseTargetLock

Libera um bloqueio em um destino.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReleaseTargetLock(
  [in] IUnknown *pContext
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pContext* \[ no\]
</dt> <dd>

Um ponteiro para o contexto retornado pelo método [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método só está disponível no Windows Server 2012 R2 com [KB3091411](https://support.microsoft.com/kb/3091411) instalado na interface [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) . Esse método está disponível na interface [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) a partir do Windows Server 2016.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                             |
| Fim do suporte do servidor<br/>    | Windows Server 2012 R2<br/>                                                             |
| INSERI<br/>                      | <dl> <dt>SbTsV. idl</dt> </dl>          |
| IID<br/>                      | IID \_ ITsSbResourcePluginStoreEx é definido como 80b83ffd-625d-11e5-bea1-a0481c7e9064<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md)
</dt> </dl>

 

 





