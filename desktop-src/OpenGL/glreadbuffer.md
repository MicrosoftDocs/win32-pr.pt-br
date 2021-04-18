---
title: função glReadBuffer (GL. h)
description: A função glReadBuffer seleciona uma fonte de buffer de cores para pixels.
ms.assetid: 734153fa-e809-4b70-867e-55e46ab95712
keywords:
- função glReadBuffer OpenGL
topic_type:
- apiref
api_name:
- glReadBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f0e88cdcb2b1b3257b23606f8160e0986584db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758032"
---
# <a name="glreadbuffer-function"></a>função glReadBuffer

A função **glReadBuffer** seleciona uma fonte de buffer de cores para pixels.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glReadBuffer(
   GLenum mode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mode* 
</dt> <dd>

Um buffer de cores. Os valores aceitos são GL \_ frontal \_ esquerdo, GL \_ frontal \_ direito, GL \_ traseiro \_ esquerdo, GL \_ traseiro \_ direito, GL \_ frontal, GL \_ voltar, GL \_ Left, GL \_ direito e GL \_ aux *i*, onde *estou* entre 0 e GL \_ \_ buffers Aux 1.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *modo* não era um dos doze (ou mais) valores aceitos.<br/>                                                             |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | o *modo* especificou um buffer que não existe.<br/>                                                                             |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glReadBuffer** especifica um buffer de cores como a origem para os comandos [**glReadPixels**](glreadpixels.md) e [**glCopyPixels**](glcopypixels.md) subsequentes. O parâmetro *Mode* aceita um de doze ou mais valores predefinidos. (GL \_ AUX0 por meio do GL \_ AUX3 são sempre definidos.) Em um sistema totalmente configurado, \_ o GL frontal, GL \_ Left e GL \_ front \_ Left, todos os nomes o buffer frontal esquerdo, o GL \_ front \_ Right e GL \_ Right Name o buffer frontal direito, e GL \_ back \_ Left e GL \_ back name The Back-Left buffer.

As configurações de buffer duplo não estéreo têm apenas um buffer frontal esquerdo e um back-Left. Configurações de buffer único têm um buffer front-Left e um front-Right se estéreo e apenas um buffer de front-Left se não estéreo. É um erro especificar um buffer inexistente para **glReadBuffer**.

Por padrão, o *modo* é GL \_ frontal em configurações de buffer único e o GL \_ volta em configurações de buffer duplo.

A função a seguir recupera informações relacionadas a **glReadBuffer**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ buffer de leitura do argumento GL \_

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> </dl>

 

 





