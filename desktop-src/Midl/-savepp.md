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
ms.openlocfilehash: c574d1032d9e392973478bc1df1e22cde6a49145b6f4775d928aac0b35e6988b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067476"
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

 

 




