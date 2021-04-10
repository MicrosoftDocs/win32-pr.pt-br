---
title: Makefiles
description: Os makefiles para cada um dos exemplos de código nesta série são os makefiles genéricos do Microsoft Win32 e devem ser criados na janela de prompt de comando.
ms.assetid: f9944069-b536-4ae2-8411-f02c3a78978c
keywords:
- Armazenamento estruturado de makefiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a15fef5818c28986232e8c2a648f43bdc096832f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292873"
---
# <a name="makefiles"></a>Makefiles

Os makefiles para cada um dos exemplos de código nesta série são os makefiles genéricos do Microsoft Win32 e devem ser criados na janela de prompt de comando. Eles assumem as ferramentas de compilador e vinculador da Microsoft e, provavelmente, exigirão alguma modificação para trabalhar com outras ferramentas. A maioria das opções de linha de comando do compilador/vinculador é especificada por macros definidas no arquivo Makefile do Win32. Mak incluído no SDK (Software Development Kit) da plataforma.

O arquivo de Makeall.bat e cada respectivo Makefile de exemplo de código, dão suporte a opções comuns, listadas na tabela a seguir, para invocação na janela de prompt de comando para controlar a natureza da compilação.



| Invocação de NMAKE        | Invocação de Makeall          | Efeito                       |
|-------------------------|-----------------------------|------------------------------|
| **NMAKE**               | **makeall**                 | Compilar com informações de depuração.     |
| **NMAKE** **NODEBUG = 1** | **makeall** **"NODEBUG = 1"** | Compilar sem informações de depuração.  |
| Perfil de **NMAKE** **= 1** | **makeall** **"Profile = 1"** | Compile com informações de criação de perfil. |
| ajuste **NMAKE** **= 1**    | **makeall** **"ajustar = 1"**    | Com informações de sintonizador de conjunto de trabalho. |
| **NMAKE** **Unicode = 1** | **makeall** **"Unicode = 1"** | Compilar para Unicode.         |
| **NMAKE** **limpar**     | **makeall** **limpar**       | Excluir binários temporários.   |
| **NMAKE** **cleanall**  | **makeall** **cleanall**    | Exclua todos os arquivos gerados.  |



 

Para as invocações de Makeall.bat, você deve ter as aspas, conforme mostrado. As opções **NODEBUG**, **Profile** e **ajuste** são mutuamente exclusivas: você pode usar apenas uma delas, ou nenhuma, para uma determinada compilação/link. Para compilar os exemplos a serem executados com cadeias de caracteres Unicode, use a opção **"Unicode = 1"** . O padrão é compilar para o suporte de cadeia de caracteres ANSI tradicional, pois você pode executar em qualquer sistema operacional Windows de 32 bits. Você pode compilar e executar livremente com ou sem Unicode no Windows Server 2003 e posterior e no Windows 2000 e posterior. Lembre-se de que o APPUTIL é sempre compilado com as mesmas opções que os outros exemplos de código que você pode estar compilando separadamente. Isso é especialmente verdadeiro para a opção **"Unicode = 1"** .

Você pode usar um IDE (ambiente de desenvolvimento integrado) do C++ de 32 bits instalado para criar os exemplos usando os makefiles genéricos fornecidos. Para isso, é necessário que o seu IDE manipule os makefiles genéricos como makefiles "externos". Os makefiles fornecidos exigem um utilitário make compatível com Microsoft NMAKE.

A maioria das IDEs de C++ pode reconhecer esses makefiles como externos e ainda fornecer muitos benefícios de edição de compilação e depuração do IDE. Por exemplo, no Microsoft Visual Studio 97 ou posterior, você pode usar a opção abrir espaço de trabalho do menu arquivo para produzir um espaço de trabalho abrindo uma cópia apropriadamente nomeada (por exemplo, Exeskel. Mak) do makefile Win32 de exemplo de código.

 

 




