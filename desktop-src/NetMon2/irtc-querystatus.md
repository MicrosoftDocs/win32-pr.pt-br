---
description: O método QueryStatus recupera o status do NPP.
ms.assetid: 4517eb34-087a-491c-97b5-cbe9190fa7a2
title: 'Método IRTC:: QueryStatus (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: e05120353cd39db661cf1b4309353034c184cd66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750582"
---
# <a name="irtcquerystatus-method"></a>Método IRTC:: QueryStatus

O método **QueryStatus** recupera o status do NPP.

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

Ponteiro para uma estrutura [NETWORKSTATUS](networkstatus.md) retornada que indica o estado atual (captura, pausa, parada e assim por diante) do NPP. É responsabilidade do aplicativo alocar e liberar a memória para a estrutura **NETWORKSTATUS** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será o seguinte código de erro:



| Código de retorno                                                                                              | Descrição                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ \_ parâmetro inválido**</dt> </dl> | O parâmetro *pNetworkStatus* não está apontando para uma estrutura [NETWORKSTATUS](networkstatus.md) válida. Aloque memória para essa estrutura e chame **IRTC:: QueryStatus** novamente.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método pode ser chamado a qualquer momento depois que o método [CreateNPPInterface](createnppinterface.md) é chamado. Você pode chamar esse método para ver se o NPP está conectado à rede, para descobrir o status da captura atual e para ver se há gatilhos pendentes. No entanto, antes de chamar esse método, você deve alocar a memória necessária para a estrutura [NETWORKSTATUS](networkstatus.md) e liberar essa memória quando a estrutura não for mais necessária.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[CreateNPPInterface](createnppinterface.md)
</dt> <dt>

[NETWORKSTATUS](networkstatus.md)
</dt> </dl>

 

 




