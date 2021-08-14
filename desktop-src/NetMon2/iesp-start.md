---
description: Método I LTD::Start – o método Start inicia uma captura.
ms.assetid: 8bf8c0c7-20be-4404-8ea5-b28b4c658523
title: Método I LTD::Start (Netmon.h)
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
ms.openlocfilehash: 8023b9db00834b10fcce84510df5ccbafec0c7a2f6654ef73d71754e7c563044
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365576"
---
# <a name="iespstart-method"></a>Método I LTD::Start

O **método Start** inicia uma captura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFileName* \[ out\]
</dt> <dd>

Ponteiro para o nome do arquivo [*de captura*](c.md) usado para armazenar os dados de rede. Certifique-se de armazenar esse nome de arquivo em cache se ele for necessário para referência futura.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será NMERR \_ SUCCESS.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                           | Descrição                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CAPTURA NMERR \_ \_ PAUSADA**</dt> </dl> | A captura está em pausa e deve ser interrompida antes que possa ser reiniciada. Chame [I LTD::Stop](iesp-stop.md) para interromper a captura.<br/> |
| <dl> <dt>**CAPTURA DE \_ NMERR**</dt> </dl>       | A captura já foi iniciada.<br/>                                                                                             |
| <dl> <dt>**NMERR \_ NÃO \_ CONECTADO**</dt> </dl>  | O NPP não está conectado à rede. Chame [I LTD::Conexão](iesp-connect.md) para conectar o NPP à rede.<br/>          |
| <dl> <dt>**NMERR \_ NOT \_ ESP**</dt> </dl>        | O NPP está conectado à rede, mas não ao [método I LTD::Conexão.](iesp-connect.md)<br/>                              |



 

## <a name="remarks"></a>Comentários

O local do arquivo [*de captura*](c.md) é especificado no registro Windows, mas você pode usar Monitor de Rede para alterar o local do diretório.

Ao reiniciar a captura usando os métodos I LTD::Start e [I RECONFIGUR::Stop,](iesp-stop.md) você deve chamar o método [I RECONFIGUR::Configure](iesp-configure.md) para reconfigurar a conexão sempre que chamar I RECONFIGUR::Start para reiniciar a captura de dados. Quando você inicia e para a captura com esses três métodos, um novo arquivo de captura é criado sempre que a captura é iniciada.

> [!Note]  
> Você também pode iniciar e parar a captura usando os métodos [I LTD::P ause](iesp-pause.md) e [I LTD::Resume.](iesp-resume.md) Quando esses dois métodos são usados, os dados capturados são armazenados no mesmo arquivo de captura.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[I LTDA](iesp.md)
</dt> <dt>

[IRIA::Configure](iesp-configure.md)
</dt> <dt>

[I LTD::Conexão](iesp-connect.md)
</dt> <dt>

[I LTD::P ause](iesp-pause.md)
</dt> <dt>

[I LTD::Resume](iesp-resume.md)
</dt> <dt>

[IRIA::Stop](iesp-stop.md)
</dt> </dl>

 

 




