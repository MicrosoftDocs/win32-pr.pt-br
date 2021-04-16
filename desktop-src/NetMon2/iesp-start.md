---
description: O método Start inicia uma captura.
ms.assetid: 8bf8c0c7-20be-4404-8ea5-b28b4c658523
title: 'Método IESP:: Start (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 2d9fc3a75fc82964f6fc5a5660ef77414ae065d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811078"
---
# <a name="iespstart-method"></a>Método IESP:: Start

O método **Start** inicia uma captura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFileName* \[ fora\]
</dt> <dd>

Ponteiro para o nome do [*arquivo de captura*](c.md) usado para armazenar os dados da rede. Certifique-se de armazenar esse nome de arquivo em cache se for necessário para referência futura.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                           | Descrição                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**captura de NMERR \_ \_ pausada**</dt> </dl> | A captura está pausada e deve ser interrompida para que possa ser reiniciada. Chame [IESP:: Stop](iesp-stop.md) para interromper a captura.<br/> |
| <dl> <dt>**captura de NMERR \_**</dt> </dl>       | A captura já foi iniciada.<br/>                                                                                             |
| <dl> <dt>**NMERR \_ não \_ conectado**</dt> </dl>  | O NPP não está conectado à rede. Chame [IESP:: Connect](iesp-connect.md) para conectar o NPP à rede.<br/>          |
| <dl> <dt>**NMERR \_ não \_ ESP**</dt> </dl>        | O NPP está conectado à rede, mas não com o método [IESP:: Connect](iesp-connect.md) .<br/>                              |



 

## <a name="remarks"></a>Comentários

O local do [*arquivo de captura*](c.md) é especificado no registro do Windows, mas você pode usar monitor de rede para alterar o local do diretório.

Ao reiniciar a captura usando os métodos IESP:: Start e [IESP:: Stop](iesp-stop.md) , você deve chamar o método [IESP:: Configure](iesp-configure.md) para reconfigurar a conexão cada vez que chamar IESP:: Start para reiniciar a captura de dados. Quando você inicia e interrompe a captura com esses três métodos, um novo arquivo de captura é criado toda vez que a captura é iniciada.

> [!Note]  
> Você também pode iniciar e parar a captura usando os métodos [IESP::P ause](iesp-pause.md) e [IESP:: resume](iesp-resume.md) . Quando esses dois métodos são usados, os dados capturados são armazenados no mesmo arquivo de captura.

 

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

[IESP:: configurar](iesp-configure.md)
</dt> <dt>

[IESP:: conectar](iesp-connect.md)
</dt> <dt>

[IESP::P ause](iesp-pause.md)
</dt> <dt>

[IESP:: retomar](iesp-resume.md)
</dt> <dt>

[IESP:: Stop](iesp-stop.md)
</dt> </dl>

 

 




