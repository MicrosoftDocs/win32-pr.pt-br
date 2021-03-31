---
title: Saída do compilador MIDL
description: Com os arquivos IDL e ACF como entrada, o compilador MIDL gera até cinco arquivos de origem em linguagem C.
ms.assetid: 151bd643-1da0-4b33-b8a3-3d7037e63319
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebb45bb369ea9d5faa695bf2658f3bafe2b3cb3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005152"
---
# <a name="midl-compiler-output"></a>Saída do compilador MIDL

Com os arquivos IDL e ACF como entrada, o compilador MIDL gera até cinco arquivos de origem em linguagem C. Por padrão, o compilador MIDL usa o nome de arquivo base do arquivo IDL como parte dos arquivos stub gerados. Quando mais de seis caracteres estão presentes no nome do arquivo base, alguns sistemas de arquivos podem não aceitar o nome completo do stub. A tabela a seguir mostra as convenções usadas para nomes de arquivo.



| Arquivo        | Parte padrão do nome do arquivo base | Exemplo      |
|-------------|-----------------------------------|--------------|
| Arquivo IDL    | ---                               | Abcdefgh. idl |
| parâmetro      | .h                                | Abcdef. h     |
| Stub do cliente | \_c. c                             | Abcdef \_ c. c  |
| Stub de servidor | \_s. c                             | Abcdef \_ s. c  |



 

 

 




