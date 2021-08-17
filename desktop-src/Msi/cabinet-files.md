---
description: Um gabinete é um único arquivo, geralmente com uma extensão .cab, que armazena arquivos compactados em uma biblioteca de arquivos.
ms.assetid: df240302-b875-49bf-8e62-7a35204c35fb
title: Arquivos de gabinete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2331b60c42bf975856987d1e13d67c95bc01fa685f99f49543650c48347cac49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380705"
---
# <a name="cabinet-files"></a>Arquivos de gabinete

Um gabinete é um único arquivo, geralmente com uma extensão .cab, que armazena arquivos compactados em uma biblioteca de arquivos. O formato de gabinete é uma maneira eficiente de empacotar vários arquivos porque a compactação é executada entre limites de arquivo, o que melhora significativamente a taxa de compactação.

Os desenvolvedores podem usar uma ferramenta de criação de arquivo de gabinete, como Makecab.exe para criar arquivos de gabinete para uso com pacotes do instalador. O Makecab.exe utilitário está incluído nos componentes [do SDK do Windows para desenvolvedores Windows instalador.](platform-sdk-components-for-windows-installer-developers.md)

Os desenvolvedores também podem usar uma ferramenta de criação de arquivo de gabinete, como Cabarc.exe para fazer arquivos de gabinete para uso com pacotes do instalador. Essa ferramenta grava na estrutura de gabinete do Diamond.

As chaves de arquivo dos arquivos armazenados dentro de um arquivo [](file-table.md) de gabinete devem corresponder às entradas na coluna Arquivo da tabela Arquivo e a sequência de arquivos no gabinete deve corresponder à sequência de arquivos especificada na coluna Sequência. Para obter mais informações, consulte [Usando gabinetes e fontes compactadas](using-cabinets-and-compressed-sources.md).

Arquivos grandes podem ser divididos entre dois ou mais arquivos de gabinete. Não pode haver mais de 15 arquivos em qualquer arquivo de gabinete que se estendo ao próximo arquivo de gabinete. Por exemplo, se você tiver três arquivos de gabinete, o primeiro gabinete poderá ter 15 arquivos que abrangem o segundo arquivo de gabinete e o segundo arquivo de gabinete poderá ter 15 arquivos que abrangem o terceiro arquivo de gabinete.

O instalador extrai arquivos de um gabinete conforme necessários para a instalação e os instala na mesma ordem em que são armazenados no arquivo de gabinete. Os requisitos de espaço para instalar um arquivo armazenado em um gabinete não são diferentes de instalar um arquivo descompactado.

Um arquivo de gabinete pode ser localizado dentro ou fora do arquivo .msi arquivo. A partir do Windows Installer 5.0 em execução no Windows 7 ou no Windows Server 2008 R2, o instalador salva todos os gabinetes inseridos no arquivo .msi antes de colocar o pacote de instalação em cache.

**[Windows Instalador 4.5 ou anterior:](not-supported-in-windows-installer-4-5.md)** Para conservar o espaço em disco, o instalador sempre remove todos os gabinetes inseridos no arquivo .msi antes de colocar o pacote de instalação em cache no computador do usuário.

 

 



