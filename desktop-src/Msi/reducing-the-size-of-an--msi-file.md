---
description: os desenvolvedores de Windows Installer pacotes podem observar seus arquivos de .msi ficando maiores do que o esperado após edições e salvações repetidas.
ms.assetid: d5229ef5-0cb5-4daf-8468-0cb653029c1c
title: Reduzindo o tamanho de um arquivo de .msi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b41cfeb949299ff4d80147fe09437cbfd708a4279bb43189c2528c495eb391
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534085"
---
# <a name="reducing-the-size-of-an-msi-file"></a>Reduzindo o tamanho de um arquivo de .msi

os desenvolvedores de Windows Installer pacotes podem observar seus arquivos de .msi ficando maiores do que o esperado após edições e salvações repetidas. Windows Os arquivos do instalador .msi são arquivos compostos que contêm armazenamentos e fluxos e têm algumas das mesmas limitações de armazenamento que os arquivos de documento OLE. Se você editar e salvar o mesmo arquivo de .msi repetidamente, ele criará espaço de armazenamento desperdiçado no arquivo. isso afeta somente os autores de .msi arquivos e não tem nenhum efeito sobre Windows Installer usuários. Os desenvolvedores podem querer remover esse espaço de armazenamento desperdiçado antes de enviar seu arquivo de .msi final.

Para remover o espaço de armazenamento desperdiçado e reduzir o tamanho final dos arquivos de .msi, você tem as seguintes opções.

-   Exporte todas as tabelas no banco de dados para arquivos. IDT e, em seguida, importe-as para um novo banco de dados. Isso produz o armazenamento mais compacto possível.
-   Use um utilitário de software para compactar o espaço de armazenamento de arquivos de documento OLE.

 

 



