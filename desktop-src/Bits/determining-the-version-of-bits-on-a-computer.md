---
title: Determinando a versão do BITS em um computador
description: Para determinar a versão do BITS no computador cliente, verifique a versão do QMgr.dll.
ms.assetid: b6057ae4-3bf0-4304-ae50-5da5e82a0bed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c94e151608511ec59e52befdef6e4f63e44476e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635022"
---
# <a name="determining-the-version-of-bits-on-a-computer"></a>Determinando a versão do BITS em um computador

Para determinar a versão do BITS no computador cliente, verifique a versão do QMgr.dll. Para localizar o número de versão da DLL:

-   Localize QMgr.dll em% windir% \\ System32.
-   Clique com o botão direito do mouse em QMgr.dll e clique em **Propriedades**.
-   Clique na guia **versão** .
-   Observe o número de versão.

Você também pode usar o seguinte código do PowerShell para determinar a versão do. dll no seu sistema:

`get-item "C:\Windows\System32\qmgr.dll" | Select-Object -ExpandProperty VersionInfo`

Se a DLL também existir em% windir% \\ System32 \\ bits, repita as etapas anteriores. O BITS usa a DLL com o número de versão mais alto.

A tabela a seguir lista as versões do BITS e seus números de versão de arquivo QMgr.dll correspondentes.



| Versão do BITS | Número de versão do arquivo QMgr.dll |
|--------------|------------------------------|
| BITS 10,1    | 7.8. xxxx. xxxx                |
| BITS 5,0     | 7.7. xxxx. xxxx                |
| BITS 4,0     | 7.5. xxxx. xxxx                |
| BITS 3,0     | 7.0. xxxx. xxxx                |
| BITS 2,5     | 6.7. xxxx. xxxx                |
| BITS 2,0     | 6.6. xxxx. xxxx                |
| BITS 1,5     | 6.5. xxxx. xxxx                |
| BITS 1,2     | 6.2. xxxx. xxxx                |
| BITS 1,0     | 6.0. xxxx. xxxx                |



 

Você também pode usar os identificadores de classe simbólicos para determinar a versão do BITS que está registrada no computador. A tabela a seguir lista as versões do BITS e seus identificadores de classe simbólico correspondentes. A função **CoCreateInstance** retornará **REGDB \_ E \_ CLASSNOTREG** se a classe não estiver registrada.



| Versão do BITS  | Identificador de classe simbólico         |
|---------------|-----------------------------------|
| BITS 10,1     | CLSID \_ BackgroundCopyManager10 \_ 1 |
| BITS 5,0      | CLSID \_ BackgroundCopyManager5 \_ 0  |
| BITS 4,0      | CLSID \_ BackgroundCopyManager4 \_ 0  |
| BITS 3,0      | CLSID \_ BackgroundCopyManager3 \_ 0  |
| BITS 2,5      | CLSID \_ BackgroundCopyManager2 \_ 5  |
| BITS 2,0      | CLSID \_ BackgroundCopyManager2 \_ 0  |
| BITS 1,5      | CLSID \_ BackgroundCopyManager1 \_ 5  |
| BITS 1,2, 1,0 | \_BACKGROUNDCOPYMANAGER CLSID      |



 

 

 




