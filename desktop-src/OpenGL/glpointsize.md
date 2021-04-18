---
title: função glPointSize (GL. h)
description: A função glPointSize especifica o diâmetro de pontos rasterizados.
ms.assetid: efa35fa8-721a-48e5-bf59-d33b9bbe7f73
keywords:
- função glPointSize OpenGL
topic_type:
- apiref
api_name:
- glPointSize
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e6b9525e302cad1eb940184eb5eb83e11744bba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756395"
---
# <a name="glpointsize-function"></a>função glPointSize

A função **glPointSize** especifica o diâmetro de pontos rasterizados.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glPointSize(
   GLfloat size
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*size* 
</dt> <dd>

O diâmetro de pontos rasterizados. O padrão é 1.0.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | o *tamanho* era menor ou igual a zero.<br/>                                                                                     |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glPointSize** especifica o diâmetro rasterizado de pontos com alias e com alias. O uso de um tamanho de ponto diferente de 1,0 tem efeitos diferentes, dependendo se a suavização de ponto está habilitada. A suavização de ponto é controlada chamando [**glEnable**](glenable.md) e **glDisable** com o argumento GL de \_ ponto \_ .

Se a suavização de ponto estiver desabilitada, o tamanho real será determinado arredondando o tamanho fornecido para o número inteiro mais próximo. (Se o arredondamento resultar no valor 0, será como se o tamanho do ponto fosse 1.) Se o tamanho arredondado for ímpar, o ponto central (*x*,*y*) do fragmento de pixel que representa o ponto será computado como

(*x*<sub>w</sub> + 0,5, *y*<sub>w</sub> +. 5)

onde *os* subscritos indicam as coordenadas da janela. Todos os pixels que estão dentro da grade quadrada do tamanho arredondado em (*x*,*y*) compõem o fragmento. Se o tamanho for par, o ponto central será

(*x*<sub>w</sub> + 0,5, *y*<sub>w</sub> +. 5)

e os centros do fragmento rasterizado são as coordenadas da janela de metade do inteiro dentro do quadrado do tamanho arredondado centralizado em (*x*,*y*). Todos os fragmentos de pixel produzidos na rasterização de um ponto de nonantialiased são atribuídos aos mesmos dados associados; o do vértice correspondente ao ponto.

Se a suavização estiver habilitada, a rasterização de ponto produzirá um fragmento para cada quadrado de pixel que interseccionará a região em que o círculo tem o diâmetro igual ao tamanho do ponto atual e centralizado nos pontos (*x*<sub>w</sub> ,*y*<sub>w</sub> ). O valor de cobertura para cada fragmento é a área de coordenadas da janela da interseção da região circular com o quadrado de pixel correspondente. Esse valor é salvo e usado na etapa de rasterização final. Os dados associados a cada fragmento são os dados associados ao ponto que está sendo rasterizado.

Nem todos os tamanhos têm suporte quando a suavização de ponto está habilitada. Se um tamanho sem suporte for solicitado, o tamanho mais próximo com suporte será usado. Há garantia de suporte apenas para o tamanho 1,0; outras dependem da implementação. O intervalo de tamanhos com suporte e a diferença de tamanho entre os tamanhos com suporte dentro do intervalo pode ser consultado chamando [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Arguments GL \_ \_ \_ intervalo de tamanho de ponto e \_ granularidade de tamanho de ponto GL \_ \_ .

O tamanho do ponto especificado por **glPointSize** sempre é retornado quando o \_ tamanho do ponto GL \_ é consultado. Fixação MSS e arredondamento para pontos com alias e sem alias não têm efeito sobre o valor especificado.

O tamanho de ponto sem alias pode ser clamped a um máximo dependente de implementação. Embora esse máximo não possa ser consultado, ele não deve ser menor que o valor máximo para pontos AntiAlias, arredondado para o valor inteiro mais próximo.

As funções a seguir recuperam informações relacionadas ao **glPointSize**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ tamanho do ponto GL do argumento \_

intervalo de tamanho de ponto de **glGet** com Argument GL \_ \_ \_

**glGet** com a \_ granularidade do \_ tamanho do ponto GL do argumento \_

[**glIsEnabled**](glisenabled.md) com o argumento GL \_ Point \_ suavizar

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

 

 





