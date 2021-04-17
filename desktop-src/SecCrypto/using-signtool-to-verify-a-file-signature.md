---
description: Explica como usar SignTool para verificar uma assinatura de arquivo.
ms.assetid: 9c40a397-19ea-4600-97ee-987dd10f4ef8
title: Usando SignTool para verificar uma assinatura de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8161d4c890400f3aa33b415e7ac16a5306aa094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750738"
---
# <a name="using-signtool-to-verify-a-file-signature"></a>Usando SignTool para verificar uma assinatura de arquivo

O comando a seguir verifica a assinatura de um arquivo chamado *MyControl.exe*:

**Verificação de SignTool** *MyControl.exe*

Se o exemplo anterior falhar, pode ser que a assinatura usou um certificado de assinatura de código. O padrão de [SignTool](signtool.md) é a política de driver do Windows para verificação.

O comando a seguir verifica a assinatura, usando a política de verificação de autenticação padrão:

**Verificação de SignTool/pa** *MyControl.exe*

O comando a seguir verifica um arquivo do sistema que pode ser assinado em um catálogo:

**SignTool Verify/a** *SysFile.dll*

O comando a seguir verifica um arquivo de sistema que está assinado em um catálogo chamado *MyCat.Cat*:

**Verificação de SignTool/c** *MyCat.catMyFile.ini*

Para qualquer verificação de [SignTool](signtool.md) , você pode recuperar o signatário do certificado. O comando a seguir verifica um arquivo do sistema e exibe o certificado do signatário:

**Verificação de SignTool/v** *MyControl.exe*

[SignTool](signtool.md) retorna um texto de linha de comando que declara o resultado da verificação de assinatura. Além disso, SignTool retorna um código de saída zero para execução bem-sucedida, uma para execução com falha e duas para execução concluída com avisos.

Para obter mais informações sobre [SignTool](signtool.md), consulte [SignTool](signtool.md).

 

 



