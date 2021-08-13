---
title: Componentes MIDLRT e Windows Runtime
description: Mostra como criar arquivos de metadados (.winmd) que representam a API para componentes Windows Runtime personalizados.
ms.assetid: 7830A5DB-9696-4A93-948B-51DA46A5143C
keywords:
- MIDL compiler MIDL
- MIDL compiler MIDL, MIDL e Windows Runtime Winrt
- Windows Runtime MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f827178216bbb7e78c16f2c11fa68b29b2eb50cfc0714a0ed53b02ce5bdc4ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642900"
---
# <a name="midlrt-and-windows-runtime-components"></a>Componentes MIDLRT e Windows Runtime

Mostra como criar arquivos de metadados (.winmd) que representam a API para componentes Windows Runtime personalizados.


Use o compilador MIDLRT para criar arquivos de metadados (.winmd) para seus componentes Windows Runtime personalizados.

Quando os arquivos de metadados são gerados, você pode compor-los em um pacote mais eficiente usando o utilitário MDMERGE. Para obter mais informações, consulte [MDMERGE e arquivos de metadados](mdmerge-and-metadata-files.md).


Usar MIDLRT é semelhante ao uso do compilador MIDL. Execute MIDLRT na linha de comando usando o seguinte comando:

**midlrt**  *<* **opções** _>_ **filename.idl**

em que as opções *<* representam as opções de linha de comando que você deseja usar e Filename.idl é o nome do arquivo _>_ IDL a ser compilado.


A lista a seguir mostra as opções de linha de comando que MIDLRT.EXE usa.

<dl>

[**Classe \_ /enum**](-enum-class.md)  
[**/metadata \_ dir**](-metadata-dir.md)  
[**/nomidl**](-nomidl.md)  
[**/nomd**](-nomd.md)  
[**Prefixo \_ /ns**](-ns-prefix.md)  
[**/winmd**](-winmd.md)  
[**/winrt**](-winrt.md)  
</dl>

Uma lista completa de opções e opções do compilador MIDLRT está disponível quando você usa o compilador MIDLRT [**/help**](-help-.md) e /? Interruptores. As opções são organizadas por categorias. Para obter mais informações, consulte [MidL Command-Line Reference](midl-command-line-reference.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Arquivos MDMERGE e de metadados](mdmerge-and-metadata-files.md)
</dt> </dl>

 

 




