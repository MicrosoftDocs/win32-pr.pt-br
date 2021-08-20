---
title: Método ITsSbResourcePluginStoreEx AcquireTargetLock
description: Bloqueia um destino.
ms.assetid: 76707f1d-1f13-4d81-8954-2acf05cda2cd
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método AcquireTargetLock
- Método AcquireTargetLock Serviços de Área de Trabalho Remota, interface ITsSbResourcePluginStoreEx
- Serviços de Área de Trabalho Remota de interface ITsSbResourcePluginStoreEx, método AcquireTargetLock
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx.AcquireTargetLock
api_location:
- SbTsV.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80a2ab7068ec754a89e384028f2d43989345e9801c4ededb800117d211b0f8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118128453"
---
# <a name="itssbresourcepluginstoreexacquiretargetlock-method"></a>Método ITsSbResourcePluginStoreEx:: AcquireTargetLock

Bloqueia um destino.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AcquireTargetLock(
  [in]  BSTR     targetName,
  [in]  DWORD    dwTimeout,
  [out] IUnknown **ppContext
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TargetName* \[ no\]
</dt> <dd>

O nome do destino a ser bloqueado.

</dd> <dt>

*dwTimeout* \[ no\]
</dt> <dd>

O tempo limite para a operação, em milissegundos.

</dd> <dt>

*ppContext* \[ fora\]
</dt> <dd>

Retorna um ponteiro para o contexto do bloqueio. Para liberar o bloqueio, forneça esse ponteiro para o método [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Depois que o bloqueio é adquirido, supõe-se que o thread de chamada tenha acesso exclusivo ao objeto de destino e, portanto, nenhum outro thread (dentro do mesmo computador) possa atualizá-lo. Portanto, o thread de chamada deve chamar o método [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) assim que tiver feito as atualizações necessárias para o objeto de destino.

> [!IMPORTANT]
> Esse bloqueio não impede completamente que os objetos de destino sejam modificados externamente se houver mais de um agente de conexão na implantação. O thread de chamada deve estar preparado para manipular uma falha normalmente e repetir a atualização de destino.

 

esse método está disponível no Windows Server 2012 R2 com [KB3091411](https://support.microsoft.com/kb/3091411) instalado na interface [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) .

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

 

 





