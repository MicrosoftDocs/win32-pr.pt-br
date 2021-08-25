---
title: Determinando a versão do BITS em um computador
description: Para determinar a versão do BITS no computador cliente, verifique a versão do QMgr.dll.
ms.assetid: b6057ae4-3bf0-4304-ae50-5da5e82a0bed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8caa2c501fd5f37d44becf11679debb1390aeeb9ee47bee02b43a97788493cd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005306"
---
# <a name="determining-the-version-of-bits-on-a-computer"></a>Determinando a versão do BITS em um computador

Para determinar a versão do BITS no computador cliente, verifique a versão do QMgr.dll. Para encontrar o número de versão da DLL:

-   Localize QMgr.dll em %windir% \\ System32.
-   Clique com o botão direito QMgr.dll clique em **Propriedades.**
-   Clique na **guia** Versão.
-   Observe o número de versão.

Você também pode usar o seguinte código do PowerShell para determinar a versão do .dll em seu sistema:

`get-item "C:\Windows\System32\qmgr.dll" | Select-Object -ExpandProperty VersionInfo`

Se a DLL também existir em %windir% \\ System32 \\ Bits, repita as etapas anteriores. O BITS usa a DLL com o número de versão mais alto.

A tabela a seguir lista as versões do BITS e seus números de QMgr.dll de arquivo correspondentes.



| Versão do BITS | QMgr.dll de versão do arquivo |
|--------------|------------------------------|
| BITS 10.1    | 7.8.xxxx.xxxx                |
| BITS 5.0     | 7.7.xxxx.xxxx                |
| BITS 4.0     | 7.5.xxxx.xxxx                |
| BITS 3.0     | 7.0.xxxx.xxxx                |
| BITS 2.5     | 6.7.xxxx.xxxx                |
| BITS 2.0     | 6.6.xxxx.xxxx                |
| BITS 1.5     | 6.5.xxxx.xxxx                |
| BITS 1.2     | 6.2.xxxx.xxxx                |
| BITS 1.0     | 6.0.xxxx.xxxx                |



 

Você também pode usar os identificadores de classe simbólicos para determinar a versão do BITS que está registrada no computador. A tabela a seguir lista as versões do BITS e seus identificadores de classe simbólico correspondentes. A **função CoCreateInstance retornará** **REGDB E \_ \_ CLASSNOTREG** se a classe não estiver registrada.



| Versão do BITS  | Identificador de classe simbólico         |
|---------------|-----------------------------------|
| BITS 10.1     | ClSID \_ BackgroundCopyManager10 \_ 1 |
| BITS 5.0      | ClSID \_ BackgroundCopyManager5 \_ 0  |
| BITS 4.0      | CLSID \_ BackgroundCopyManager4 \_ 0  |
| BITS 3.0      | ClSID \_ BackgroundCopyManager3 \_ 0  |
| BITS 2.5      | ClSID \_ BackgroundCopyManager2 \_ 5  |
| BITS 2.0      | ClSID \_ BackgroundCopyManager2 \_ 0  |
| BITS 1.5      | CLSID \_ BackgroundCopyManager1 \_ 5  |
| BITS 1.2, 1.0 | CLSID \_ BackgroundCopyManager      |



 

 

 




