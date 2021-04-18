---
title: Comutador/os
description: A opção/os especifica o método de modo misto para empacotar o código de stub passado entre o cliente e o servidor.
ms.assetid: dc5cafbb-dcc6-4fcb-a04f-1bc9720a13cb
keywords:
- MIDL do comutador/os
topic_type:
- apiref
api_name:
- /Os
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbbef54501e195c91bdcc0cec8045f2eec763820
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105758454"
---
# <a name="os-switch"></a>Comutador/os

A opção **/os** especifica o método de modo misto para empacotar o código de stub passado entre o cliente e o servidor.

``` syntax
midl /Os
```

## <a name="switch-options"></a>Opções de comutação

Essa opção não tem parâmetros.

## <a name="remarks"></a>Comentários

Há problemas importantes a serem considerados antes de decidir sobre o método de empacotamento de código. Esses problemas se preocupam com o tamanho e o desempenho. O compilador MIDL fornece dois métodos para empacotamento de código: modo misto (**/os**) e totalmente interpretado ([**/Oi**](-oi.md)). O método totalmente interpretado realiza marshaling de dados completamente offline. Isso reduz consideravelmente o tamanho do código stub, mas também resulta em desempenho reduzido.

Use o modo padrão MIDL **/Oicf** /robust para todas as finalidades além da compatibilidade com versões anteriores. Esse modo é o modo padrão seguro do compilador MIDL; qualquer outro modo deve ser usado somente após uma consideração cuidadosa da implicação de segurança, percebendo que extensões futuras serão implementadas somente para o modo padrão. No modo misto, o compilador empacota alguns parâmetros embutidos nos stubs gerados. Embora isso resulte em um tamanho maior de stub, ele também pode oferecer maior desempenho.

O MIDL fornece suporte completo para matrizes multidimensionais e ponteiros de dimensionamento multidimensional somente no modo [**/Oicf**](-oi.md) . Nos modos **/os** e **/Oi** , o compilador oferece suporte a casos simples, como matrizes de tamanho fixo. O uso de matrizes multidimensionais nos modos **/os** ou **/Oi** pode resultar em parâmetros que não são empacotados corretamente. A Microsoft recomenda que você use a opção de linha de comando **/Oicf** quando sua interface define parâmetros que são matrizes multidimensionais ou ponteiros com dimensionamento multidimensional.

Para definir melhor o nível de gradação em como os dados são empacotados, esta versão do RPC fornece um \[ [](optimize.md) \] atributo optimize. Esse atributo é usado como um atributo de interface ACF ou atributo de operação para selecionar o modo de marshaling.

## <a name="examples"></a>Exemplos

**MIDL/os filename. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Oi**](-oi.md)
</dt> <dt>

[**formato**](optimize.md)
</dt> <dt>

[**\_opção de formato de/// \_**](-no-format-opt.md)
</dt> </dl>

 

 




