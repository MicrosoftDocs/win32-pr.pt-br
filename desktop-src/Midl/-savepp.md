---
title: comutador/savePP
description: Quando a diretiva/savePP é especificada, o compilador MIDL não exclui a saída do pré-processador C/C++.
ms.assetid: 65a687a5-55ec-4e76-bcfc-38c0a317b85b
keywords:
- MIDL do comutador/savePP
topic_type:
- apiref
api_name:
- /savePP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d3ab7032768cacfab6415548a09def453ab4f9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006563"
---
# <a name="savepp-switch"></a>comutador/savePP

Quando a diretiva **/savePP** é especificada, o compilador MIDL não exclui a saída do pré-processador C/C++.

``` syntax
midl /savePP
```

## <a name="switch-options"></a>Opções de comutação

Essa opção não tem parâmetros.

## <a name="remarks"></a>Comentários

Essa opção permite aos desenvolvedores discernir o que está sendo analisado pelo compilador MIDL e é útil para a depuração. A saída do pré-processador é gravada em um ou mais arquivos temporários no diretório indicado pela variável de ambiente TEMP. O nome do arquivo de saída, ou arquivos, segue uma Convenção de nomenclatura de MID \* . tmp. Observe que uma única compilação pode gerar vários fluxos de entrada pré-processados; Isso ocorre porque a importação de um arquivo IDL, em oposição ao uso de **\# include**, faz com que um pré-processador separado seja executado.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ aceitar**](-cpp-opt.md)
</dt> <dt>

[/// \_ /nocpp](-no-cpp-nocpp.md)
</dt> </dl>

 

 




