---
title: Links do SIS e pontos de nova análise
description: O SIS é um driver de filtro NTFS que substitui arquivos duplicados por links de cópia em gravação (chamados de links do SIS) que apontam para um único arquivo de backup, reduzindo o disco e a sobrecarga de cache desses arquivos.
ms.assetid: 1600a9ff-413c-4059-b04c-c862f6cf8f32
keywords:
- Backup de pontos de nova análise
- Backup de armazenamento de instância única (SIS), links do SIS
- Backup de repositório de instância única (SIS), pontos de nova análise
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f89901df6ce1fea1635d4250f2884ec9baf68fb1552766564909486c8ed00a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588856"
---
# <a name="sis-links-and-reparse-points"></a>Links do SIS e pontos de nova análise

O SIS é um driver de filtro NTFS que substitui arquivos duplicados por links de cópia em gravação (chamados de links do SIS) que apontam para um único arquivo de backup, reduzindo o disco e a sobrecarga de cache desses arquivos. Esse arquivo de backup está contido em um [repositório comum](the-sis-common-store-and-common-store-files.md). A implementação da arquitetura do SIS faz uso de [pontos de nova análise](/windows/desktop/FileIO/reparse-points) que contêm informações sobre os links do SIS.

Os links do SIS são implementados como arquivos esparsos, geralmente com a maioria dos intervalos do arquivo não alocados e um ponto de nova análise. A estrutura e o conteúdo de um ponto de nova análise são opacos para seus aplicativos de backup e restauração; no entanto, seus aplicativos enviam e recuperam os dados dentro desses pontos de nova análise de e para funções de API do SIS que processam as informações neles. As informações em um ponto de nova análise referem-se a um único arquivo de backup que contém os dados de arquivo reais. Esse arquivo de backup é chamado de [arquivo de armazenamento comum](the-sis-common-store-and-common-store-files.md)e existe no repositório comum.

Ao restaurar um link do SIS, o aplicativo de restauração deve executar as seguintes etapas:

1.  Determine o arquivo de repositório comum ou os arquivos aos quais o link do SIS aponta.
2.  Se o arquivo ou os arquivos não existirem no armazenamento comum, restaure o arquivo ou os arquivos juntamente com o link do SIS.
3.  Se o link do SIS apontar para um arquivo de armazenamento comum ou arquivos que existem no disco, restaure apenas o link do SIS. Lembre-se de que os dados em arquivos de armazenamento comum nunca são alterados, portanto, se um determinado arquivo de repositório comum ainda estiver no disco no momento da restauração, ele terá o mesmo conteúdo de quando foi feito o backup e não haverá necessidade de substituí-lo.

A única sobrecarga adicional necessária para backups assistidos por SIS é que seu aplicativo de backup deve fazer backup do link do SIS e dos dados associados aos arquivos de backup. Todas as operações de backup e restauração do SIS são locais para um volume específico.

 

 