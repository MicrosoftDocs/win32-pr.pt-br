---
description: Método IDelaydC::Start – o método Start inicia uma captura.
ms.assetid: 92b25afc-d5d8-47e4-a155-4ed2a3571038
title: Método IDelaydC::Start (Netmon.h)
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
ms.openlocfilehash: 750a33241358aee924ed3f91491185117a77a548a87bdfc5514d59fe4798a42c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365861"
---
# <a name="idelaydcstart-method"></a>Método IDelaydC::Start

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



| Código de retorno                                                                                           | Descrição                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CAPTURA NMERR \_ \_ PAUSADA**</dt> </dl> | A captura está em um estado de pausa e deve ser interrompida antes que possa ser reiniciada. Chame [**IDelaydC::Stop**](idelaydc-stop.md) para interromper a captura. Para obter mais informações, consulte a seção Comentários neste tópico.<br/> |
| <dl> <dt>**CAPTURA DE \_ NMERR**</dt> </dl>       | A captura já foi iniciada.<br/>                                                                                                                                                                                 |
| <dl> <dt>**NMERR \_ NÃO \_ CONECTADO**</dt> </dl>  | O NPP não está conectado à rede. Chame [**IDelaydC::Conexão**](idelaydc-connect.md) para se conectar à rede.<br/>                                                                                          |
| <dl> <dt>**NMERR \_ NÃO \_ ATRASADO**</dt> </dl>    | O NPP está conectado à rede, mas não ao [**método IDelaydC::Conexão.**](idelaydc-connect.md)<br/>                                                                                                      |



 

## <a name="remarks"></a>Comentários

O local do arquivo [*de*](c.md) captura é especificado em seu registro Windows, mas você pode usar Monitor de Rede para alterar o local do arquivo.

Para reiniciar a captura usando **IDelaydC::Start** e [**IDelaydC::Stop**](idelaydc-stop.md), você deve chamar o método [**IDelaydC::Configure**](idelaydc-configure.md) para reconfigurar a conexão sempre que chamar o método **IDelaydC::Start** para reiniciar a captura de dados. Quando você inicia e para a captura com esses três métodos, um novo arquivo de captura é criado sempre que a captura é iniciada.

> [!Note]  
> Você também pode iniciar e parar a captura usando os métodos [**IDelaydC::P ause**](idelaydc-pause.md) e [**IDelaydC::Resume.**](idelaydc-resume.md) Quando você usa esses dois métodos, os dados capturados são armazenados no mesmo arquivo de captura.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[**IDelaydC::Configure**](idelaydc-configure.md)
</dt> <dt>

[**IDelaydC::Conexão**](idelaydc-connect.md)
</dt> <dt>

[**IDelaydC::P ause**](idelaydc-pause.md)
</dt> <dt>

[**IDelaydC::Resume**](idelaydc-resume.md)
</dt> <dt>

[**IDelaydC::Stop**](idelaydc-stop.md)
</dt> </dl>

 

 




