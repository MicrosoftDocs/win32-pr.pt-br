---
description: Explica como usar SignTool para verificar uma assinatura de arquivo.
ms.assetid: 9c40a397-19ea-4600-97ee-987dd10f4ef8
title: Usando SignTool para verificar uma assinatura de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e91df7a64a8db48d04ceba9df5fbc3fd358058
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/25/2021
ms.locfileid: "107954919"
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

**SignTool Verify/c** *MyCat.Cat* *MyFile.ini*

Para qualquer verificação de [SignTool](signtool.md) , você pode recuperar o signatário do certificado. O comando a seguir verifica um arquivo do sistema e exibe o certificado do signatário:

**Verificação de SignTool/v** *MyControl.exe*

[SignTool](signtool.md) retorna um texto de linha de comando que declara o resultado da verificação de assinatura. Além disso, SignTool retorna um código de saída zero para execução bem-sucedida, uma para execução com falha e duas para execução concluída com avisos.

Para obter mais informações sobre [SignTool](signtool.md), consulte [SignTool](signtool.md).

 

 



