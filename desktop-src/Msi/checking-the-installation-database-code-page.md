---
description: Uma página de código é uma tabela interna que o sistema operacional usa para mapear símbolos (letras, numerais e caracteres de pontuação) para um número de caractere.
ms.assetid: e11193a2-2c72-43a9-8d35-fa524044e306
title: Verificando a página de código do banco de dados de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cedb63128d4a3b18878eba16af5e55da92403953ddf2a2c9a29c788a524ad41f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581766"
---
# <a name="checking-the-installation-database-code-page"></a>Verificando a página de código do banco de dados de instalação

Uma *página de código* é uma tabela interna que o sistema operacional usa para mapear símbolos (letras, numerais e caracteres de pontuação) para um número de caractere. Páginas de código diferentes fornecem suporte para os conjuntos de caracteres usados em diferentes países ou regiões. As páginas de código são referenciadas por número; por exemplo, a página de código 932 representa o conjunto de caracteres japonês e a página de código 950 representa um dos conjuntos de caracteres chineses. Consulte [Localizando as tabelas Error e ActionText](localizing-the-error-and-actiontext-tables.md) para ver uma lista de páginas de código ASCII.

A mesma página de código ASCII, 1252, pode ser usada para inglês e francês. Portanto, a página de código do banco de MNP2000.msi (inglês) não precisa ser redefinida para alterar a instalação para francês.

Para obter mais informações sobre como definir a página de código, consulte Tratamento de página de [código (Windows Instalador)](code-page-handling-windows-installer-.md).

[Continuar](importing-localized-error-and-actiontext-tables.md)

 

 



