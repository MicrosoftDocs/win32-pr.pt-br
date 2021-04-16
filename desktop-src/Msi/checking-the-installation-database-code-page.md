---
description: Uma página de código é uma tabela interna que o sistema operacional usa para mapear símbolos (letras, numerais e caracteres de pontuação) para um número de caractere.
ms.assetid: e11193a2-2c72-43a9-8d35-fa524044e306
title: Verificando a página de código do banco de dados de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ea9513ec80413e00a9f3f4c1232a06704f83e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757527"
---
# <a name="checking-the-installation-database-code-page"></a>Verificando a página de código do banco de dados de instalação

Uma *página de código* é uma tabela interna que o sistema operacional usa para mapear símbolos (letras, numerais e caracteres de pontuação) para um número de caractere. Páginas de código diferentes fornecem suporte para os conjuntos de caracteres usados em diferentes países ou regiões. As páginas de código são referenciadas por número; por exemplo, a página de código 932 representa o conjunto de caracteres japoneses e a página de código 950 representa um dos conjuntos de caracteres chineses. Consulte [localizando as tabelas Error e ActionText](localizing-the-error-and-actiontext-tables.md) para obter uma lista de páginas de código ASCII.

A mesma página de código ASCII, 1252, pode ser usada para inglês e francês. Portanto, a página de código para o banco de dados MNP2000.msi (inglês) não precisa ser redefinida para alterar a instalação para francês.

Para obter mais informações sobre como definir a página de código, consulte [manipulação de página de código (Windows Installer)](code-page-handling-windows-installer-.md).

[Continuar](importing-localized-error-and-actiontext-tables.md)

 

 



