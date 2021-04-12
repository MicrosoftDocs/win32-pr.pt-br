---
title: Componentes MIDLRT e Windows Runtime
description: Mostra como criar arquivos de metadados (. winmd) que representam a API para componentes de Windows Runtime personalizados.
ms.assetid: 7830A5DB-9696-4A93-948B-51DA46A5143C
keywords:
- MIDL do compilador MIDL
- MIDL do compilador MIDL, MIDL e Windows Runtime winrt
- MIDL de Windows Runtime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edf4d40b3fc5b0a5ed8eeb9b5fd47a3b87c4543
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104499187"
---
# <a name="midlrt-and-windows-runtime-components"></a>Componentes MIDLRT e Windows Runtime

Mostra como criar arquivos de metadados (. winmd) que representam a API para componentes de Windows Runtime personalizados.


Use o compilador MIDLRT para compilar arquivos de metadados (. winmd) para seus componentes de Windows Runtime personalizados.

Quando os arquivos de metadados são gerados, você pode redação-los em um pacote mais eficiente usando o utilitário MDMERGE. Para obter mais informações, consulte [MDMERGE e arquivos de metadados](mdmerge-and-metadata-files.md).


O uso de MIDLRT é semelhante ao uso do compilador MIDL. Execute MIDLRT na linha de comando usando o seguinte comando:

**midlrt**  *<* **Opções** _>_ do **nome do arquivo. idl**

onde **as opções** * < * _>_ representam as opções de linha de comando que você deseja usar e filename. idl é o nome do arquivo IDL a ser compilado.


A lista a seguir mostra as opções de linha de comando que o MIDLRT.EXE usa.

<dl>

[**\_classe/enum**](-enum-class.md)  
[**/Metadata \_ dir**](-metadata-dir.md)  
[**/nomidl**](-nomidl.md)  
[**/nomd**](-nomd.md)  
[**\_prefixo/NS**](-ns-prefix.md)  
[**/winmd**](-winmd.md)  
[**/winrt**](-winrt.md)  
</dl>

Uma lista completa dos comutadores e opções do compilador MIDLRT está disponível quando você usa o compilador MIDLRT [**/Help**](-help-.md) e/? comutadores. As opções são organizadas por categorias. Para obter mais informações, consulte a [referência de Command-Line MIDL](midl-command-line-reference.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[MDMERGE e arquivos de metadados](mdmerge-and-metadata-files.md)
</dt> </dl>

 

 




