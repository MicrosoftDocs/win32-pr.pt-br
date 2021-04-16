---
title: função glLineWidth (GL. h)
description: A função glLineWidth especifica a largura das linhas rasterizadas.
ms.assetid: 13a69fd7-5eee-42ec-bd05-5bd3c838d4d7
keywords:
- função glLineWidth OpenGL
topic_type:
- apiref
api_name:
- glLineWidth
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa4cecafc9e5d8e0f55c6e9d0dbfe49924d54f14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753955"
---
# <a name="gllinewidth-function"></a>função glLineWidth

A função **glLineWidth** especifica a largura das linhas rasterizadas.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glLineWidth(
   GLfloat width
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*width* 
</dt> <dd>

A largura das linhas rasterizadas. O padrão é 1.0.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | a *largura* era menor ou igual a zero.<br/>                                                                                    |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glLineWidth** especifica a largura rasterizada das linhas com alias e com suavização de alias. O uso de uma largura de linha diferente de 1,0 tem efeitos diferentes, dependendo se a suavização de linha está habilitada. A suavização de linha é controlada chamando [**glEnable**](glenable.md) e **glDisable** com a linha de argumento GL \_ \_ suave.

Se a suavização de linha estiver desabilitada, a largura real será determinada arredondando a largura fornecida para o número inteiro mais próximo. (Se o arredondamento resultar no valor 0,0, é como se a largura da linha fosse 1,0) Se \| ? x \|  =  \| ? y \| , *i* pixels são preenchidos em cada coluna que é rasterizada, onde *eu* é o valor arredondado da *largura*. Caso contrário, os pixels de *i* são preenchidos em cada linha rasterizada.

Se a suavização estiver habilitada, a rasterização de linha produzirá um fragmento para cada quadrado de pixel que Interseccionar a região na parte do retângulo com largura igual à largura da linha atual, comprimento igual ao comprimento real da linha e centralizado no segmento de linha matemática. O valor de cobertura para cada fragmento é a área de coordenadas da janela da interseção da região retangular com o quadrado de pixel correspondente. Esse valor é salvo e usado na etapa de rasterização final.

Nem todas as larguras podem ter suporte quando a suavização de linha está habilitada. Se uma largura sem suporte for solicitada, a largura com suporte mais próxima será usada. Há garantia de suporte apenas para a largura 1,0; outras dependem da implementação. O intervalo de larguras com suporte e a diferença de tamanho entre as larguras com suporte dentro do intervalo pode ser consultado chamando **glGet** com Arguments \_ \_ \_ e \_ granularidade de largura da linha gl \_ \_ .

A largura da linha especificada por **glLineWidth** sempre é retornada quando a \_ largura da linha gl \_ é consultada. Fixação MSS e arredondamento para linhas com alias e sem alias não têm efeito sobre o valor especificado.

A largura de linha sem alias pode ser clamped para um máximo dependente de implementação. Embora esse máximo não possa ser consultado, ele não deve ser menor que o valor máximo para linhas AntiAlias, arredondado para o valor inteiro mais próximo.

As funções a seguir recuperam informações relacionadas ao **glLineWidth**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com largura de linha do argumento GL \_ \_

**glGet** com intervalo de \_ largura de linha do argumento GL \_ \_

**glGet** com granularidade de \_ largura de linha do argumento GL \_ \_

[**glIsEnabled**](glisenabled.md) com linha de argumento GL \_ \_ suave

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

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





