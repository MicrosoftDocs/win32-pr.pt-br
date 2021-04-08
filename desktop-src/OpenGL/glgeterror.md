---
title: função glGetError (GL. h)
description: A função glGetError retorna informações de erro.
ms.assetid: 18f0368f-054f-4b84-8397-3f9ee4aa07fa
keywords:
- função glGetError OpenGL
topic_type:
- apiref
api_name:
- glGetError
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c0abf6ec03ca0c29ede3b7d396db375fd06ac6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919004"
---
# <a name="glgeterror-function"></a>função glGetError

A função **glGetError** retorna informações de erro.

## <a name="syntax"></a>Sintaxe


```C++
GLenum WINAPI glGetError(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

A função **glGetError** retorna um dos seguintes códigos de erro.



| Código de retorno                                                                                           | Descrição                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | Um valor inaceitável é especificado para um argumento enumerado. A função transgressor é ignorada, não tendo nenhum efeito colateral além de definir o sinalizador de erro.<br/>         |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | Um argumento numérico está fora do intervalo. A função transgressor é ignorada, não tendo nenhum efeito colateral além de definir o sinalizador de erro.<br/>                                    |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A operação especificada não é permitida no estado atual. A função transgressor é ignorada, não tendo nenhum efeito colateral além de definir o sinalizador de erro.<br/>           |
| <dl> <dt>**GL \_ sem \_ erro**</dt> </dl>          | Nenhum erro foi registrado. O valor dessa constante simbólica é garantido como zero.<br/>                                                                         |
| <dl> <dt>**\_estouro de pilha GL \_**</dt> </dl>    | Essa função causaria um estouro de pilha. A função transgressor é ignorada, não tendo nenhum efeito colateral além de definir o sinalizador de erro.<br/>                            |
| <dl> <dt>**\_estouro negativo de pilha GL \_**</dt> </dl>   | Essa função causaria um estouro negativo de pilha. A função transgressor é ignorada, não tendo nenhum efeito colateral além de definir o sinalizador de erro.<br/>                           |
| <dl> <dt>**GL \_ sem \_ \_ memória**</dt> </dl>    | Não há memória suficiente restante para executar a função. O estado do OpenGL é indefinido, exceto pelo Estado dos sinalizadores de erro, depois que esse erro é registrado.<br/> |



 

Observe que **glGetError** retorna GL \_ Operation inválida \_ se for chamado entre uma chamada para [**glBegin**](glbegin.md) e sua chamada correspondente para [**glEnd**](glend.md).

## <a name="remarks"></a>Comentários

Cada erro detectável é atribuído a um código numérico e a um nome simbólico. Quando ocorre um erro, o sinalizador de erro é definido como o valor do código de erro apropriado. Nenhum outro erro é registrado até que **glGetError** seja chamado, o código de erro é retornado e o sinalizador é redefinido para GL \_ sem \_ erro. Se uma chamada para **glGetError** retornar GL \_ sem \_ erro, não haverá erro detectável desde a última chamada para **GlGetError** ou desde que o OpenGL foi inicializado.

Para permitir implementações distribuídas, pode haver vários sinalizadores de erro. Se qualquer sinalizador de erro único gravou um erro, o valor desse sinalizador será retornado e esse sinalizador será redefinido como GL \_ sem \_ erro quando **glGetError** for chamado. Se mais de um sinalizador tiver registrado um erro, **glGetError** retornará e limpará um valor de sinalizador de erro arbitrário. Se todos os sinalizadores de erro forem redefinidos, você sempre deverá chamar **glGetError** em um loop até que ele retorne o GL \_ sem \_ erro.

Inicialmente, todos os sinalizadores de erro são definidos como GL \_ sem \_ erro.

Quando um sinalizador de erro é definido, os resultados de uma operação OpenGL são indefinidos somente se o GL \_ \_ \_ tiver ocorrido memória insuficiente. Em todos os outros casos, a função que gera o erro é ignorada e não tem efeito sobre o estado do OpenGL ou o conteúdo do framebuffer.

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

[**glEnd**](glend.md)
</dt> </dl>

 

 





