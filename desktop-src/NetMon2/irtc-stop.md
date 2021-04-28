---
description: 'Método IRTC:: Stop – o método Stop interrompe a captura atual.'
ms.assetid: 64a80ff1-5a48-4be8-835d-a3d304ebb324
title: 'Método IRTC:: Stop (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 10bf0886032c93288435ade05fec46077d53753c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113514"
---
# <a name="irtcstop-method"></a>Método IRTC:: Stop

O método **Stop** interrompe a captura atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                          | Descrição                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ não \_ conectado**</dt> </dl> | O NPP não está conectado à rede. Chame [IRTC:: Connect](irtc-connect.md) para conectar o NPP à rede.<br/> |
| <dl> <dt>**NMERR \_ não \_ capturando**</dt> </dl> | O NPP não está capturando dados. Chame [IRTC:: Start](irtc-start.md) para iniciar a captura.<br/>                            |
| <dl> <dt>**NMERR \_ não está em \_ tempo real**</dt> </dl>  | O NPP está conectado à rede, mas não com o método [IRTC:: Connect](irtc-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Comentários

Ao reiniciar a captura depois de chamar o método **IRTC:: Stop** , chame [IRTC:: Configure](irtc-configure.md) cada vez que você chamar [IRTC:: Start](irtc-start.md) para reiniciar a captura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC:: conectar](irtc-connect.md)
</dt> <dt>

[IRTC:: configurar](irtc-configure.md)
</dt> <dt>

[IRTC:: iniciar](irtc-start.md)
</dt> </dl>

 

 




