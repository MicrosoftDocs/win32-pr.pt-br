---
description: Um gabinete é um arquivo único, geralmente com uma extensão. cab, que armazena arquivos compactados em uma biblioteca de arquivos.
ms.assetid: df240302-b875-49bf-8e62-7a35204c35fb
title: Arquivos de gabinete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7b54ae737785abc33edd46c9e53edc93fcd288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755089"
---
# <a name="cabinet-files"></a>Arquivos de gabinete

Um gabinete é um arquivo único, geralmente com uma extensão. cab, que armazena arquivos compactados em uma biblioteca de arquivos. O formato de gabinete é uma maneira eficiente de empacotar vários arquivos, pois a compactação é executada em limites de arquivos, o que melhora significativamente a taxa de compactação.

Os desenvolvedores podem usar uma ferramenta de criação de arquivo de gabinete, como Makecab.exe para criar arquivos de gabinete para uso com pacotes do instalador. O utilitário Makecab.exe está incluído nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

Os desenvolvedores também podem usar uma ferramenta de criação de arquivo de gabinete, como Cabarc.exe para criar arquivos de gabinete para uso com pacotes do instalador. Essa ferramenta grava na estrutura de gabinete Diamond.

As chaves de arquivo dos arquivos armazenados dentro de um arquivo de gabinete devem corresponder às entradas na coluna arquivo da [tabela de arquivos](file-table.md) e a sequência de arquivos no gabinete deve corresponder à sequência de arquivos especificada na coluna sequência. Para obter mais informações, consulte [usando gabinetes e fontes compactadas](using-cabinets-and-compressed-sources.md).

Arquivos grandes podem ser divididos entre dois ou mais arquivos de gabinete. Não pode haver mais de 15 arquivos em um arquivo de gabinete que abranja o próximo arquivo de gabinete. Por exemplo, se você tiver três arquivos de gabinete, o primeiro gabinete poderá ter 15 arquivos que se estendem ao segundo arquivo de gabinete e o segundo arquivo de gabinete pode ter 15 arquivos que abrangem o terceiro arquivo de gabinete.

O instalador extrai arquivos de um gabinete conforme eles são necessários para a instalação e os instala na mesma ordem em que são armazenados no arquivo de gabinete. Os requisitos de espaço para a instalação de um arquivo armazenado em um gabinete não são diferentes de instalar um arquivo descompactado.

Um arquivo de gabinete pode ser localizado dentro ou fora do arquivo. msi. A partir do Windows Installer 5,0 em execução no Windows 7 ou no Windows Server 2008 R2, o instalador salva todos os gabinetes inseridos no arquivo. msi antes de armazenar em cache o pacote de instalação.

**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Para conservar o espaço em disco, o instalador sempre remove todos os gabinetes inseridos no arquivo. msi antes de armazenar em cache o pacote de instalação no computador do usuário.

 

 



