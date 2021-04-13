---
description: O método Disconnect desconecta o NPP da rede.
ms.assetid: 47a0cce0-a50d-4bad-9787-672cc3d13d07
title: 'IRTC: método:D isconnect (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: df58d6ac0e61ecc370510474c3bc067726d9824b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165349"
---
# <a name="irtcdisconnect-method"></a>Método IRTC::D isconnect

O método **Disconnect desconecta** o NPP da rede.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                          | Descrição                                                                                                         |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**captura de NMERR \_**</dt> </dl>      | O NPP está capturando dados. Não é possível desconectar da rede enquanto a captura de dados está em andamento.<br/> |
| <dl> <dt>**NMERR \_ não \_ conectado**</dt> </dl> | O NPP não está conectado à rede.<br/>                                                                 |
| <dl> <dt>**NMERR \_ não está em \_ tempo real**</dt> </dl>  | O NPP está conectado à rede, mas não com o método [IRTC:: Connect](irtc-connect.md) .<br/>           |



 

## <a name="remarks"></a>Comentários

Este método não pode ser chamado quando o NPP está capturando dados. Você deve chamar o método [IRTC:: Stop](irtc-stop.md) antes de chamar IRTC::D isconnect.

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

[IRTC:: conectar](irtc-connect.md)
</dt> <dt>

[IRTC:: Stop](irtc-stop.md)
</dt> </dl>

 

 




