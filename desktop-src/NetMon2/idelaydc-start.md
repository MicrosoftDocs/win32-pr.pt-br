---
description: O método Start inicia uma captura.
ms.assetid: 92b25afc-d5d8-47e4-a155-4ed2a3571038
title: 'Método IDelaydC:: Start (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: a912af44dddb8a25d3279a5cdd7f021646c26e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784173"
---
# <a name="idelaydcstart-method"></a>Método IDelaydC:: Start

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



| Código de retorno                                                                                           | Descrição                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**captura de NMERR \_ \_ pausada**</dt> </dl> | A captura está em um estado de pausa e deve ser interrompida para que possa ser reiniciada. Chame [**IDelaydC:: Stop**](idelaydc-stop.md) para interromper a captura. Para obter mais informações, consulte a seção comentários neste tópico.<br/> |
| <dl> <dt>**captura de NMERR \_**</dt> </dl>       | A captura já foi iniciada.<br/>                                                                                                                                                                                 |
| <dl> <dt>**NMERR \_ não \_ conectado**</dt> </dl>  | O NPP não está conectado à rede. Chame [**IDelaydC:: Connect**](idelaydc-connect.md) para conectar-se à rede.<br/>                                                                                          |
| <dl> <dt>**NMERR \_ não \_ atrasada**</dt> </dl>    | O NPP está conectado à rede, mas não com o método [**IDelaydC:: Connect**](idelaydc-connect.md) .<br/>                                                                                                      |



 

## <a name="remarks"></a>Comentários

O local do [*arquivo de captura*](c.md) é especificado no registro do Windows, mas você pode usar monitor de rede para alterar o local do arquivo.

Para reiniciar a captura usando **IDelaydC:: Start** e [**IDelaydC:: Stop**](idelaydc-stop.md), você deve chamar o método [**IDelaydC:: Configure**](idelaydc-configure.md) para reconfigurar a conexão cada vez que você chamar o método **IDelaydC:: Start** para reiniciar a captura de dados. Quando você inicia e interrompe a captura com esses três métodos, um novo arquivo de captura é criado toda vez que a captura é iniciada.

> [!Note]  
> Você também pode iniciar e parar a captura usando os métodos [**IDelaydC::P ause**](idelaydc-pause.md) e [**IDelaydC:: resume**](idelaydc-resume.md) . Quando você usa esses dois métodos, os dados capturados são armazenados no mesmo arquivo de captura.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[**IDelaydC:: configurar**](idelaydc-configure.md)
</dt> <dt>

[**IDelaydC:: conectar**](idelaydc-connect.md)
</dt> <dt>

[**IDelaydC::P ause**](idelaydc-pause.md)
</dt> <dt>

[**IDelaydC:: retomar**](idelaydc-resume.md)
</dt> <dt>

[**IDelaydC:: Stop**](idelaydc-stop.md)
</dt> </dl>

 

 




