---
description: Recupera o status de NPP.
ms.assetid: 48682997-f641-4ae5-b5ad-64fd84f07ae3
title: 'Método IESP:: QueryStatus (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 00b83cbbb167775a8de360c880f381b41f250abf0eab01c883bc7580be4d956f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037536"
---
# <a name="iespquerystatus-method"></a>Método IESP:: QueryStatus

O método **QueryStatus** recupera o status NPP.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pNetworkStatus* \[ fora\]
</dt> <dd>

Um ponteiro para uma estrutura [NETWORKSTATUS](networkstatus.md) retornada que indica o estado atual (captura, pausa, parada e assim por diante) do NPP. O usuário deve alocar e liberar a memória para a estrutura NETWORKSTATUS.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será o seguinte código de erro:



| Código de retorno                                                                                              | Descrição                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ \_ parâmetro inválido**</dt> </dl> | O parâmetro *pNetworkStatus* não está apontando para uma estrutura [NETWORKSTATUS](networkstatus.md) válida. Aloque memória para essa estrutura e chame **IESP:: QueryStatus** novamente.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método pode ser chamado a qualquer momento após o [CreateNPPInterface](createnppinterface.md) ser chamado. Você pode chamar esse método para ver se o NPP está conectado à rede, para descobrir o status da captura atual e para ver se há gatilhos pendentes.

Antes de chamar esse método, aloque a memória necessária para a estrutura [NETWORKSTATUS](networkstatus.md) e libere essa memória quando a estrutura não for mais necessária.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[CreateNPPInterface](createnppinterface.md)
</dt> <dt>

[NETWORKSTATUS](networkstatus.md)
</dt> </dl>

 

 




