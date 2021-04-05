---
description: Os desenvolvedores de Windows Installer pacotes podem notar seus arquivos. msi ficando maiores do que o esperado após edições e salvações repetidas.
ms.assetid: d5229ef5-0cb5-4daf-8468-0cb653029c1c
title: Reduzindo o tamanho de um arquivo. msi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b5a19c92f0567fc6081d772279ec2cc0b6cafef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921640"
---
# <a name="reducing-the-size-of-an-msi-file"></a>Reduzindo o tamanho de um arquivo. msi

Os desenvolvedores de Windows Installer pacotes podem notar seus arquivos. msi ficando maiores do que o esperado após edições e salvações repetidas. Os arquivos. msi do Windows Installer são arquivos compostos que contêm armazenamentos e fluxos e têm algumas das mesmas limitações de armazenamento que os arquivos de documento OLE. Se você editar e salvar o mesmo arquivo. msi repetidamente, ele criará o espaço de armazenamento desperdiçado no arquivo. Isso afeta apenas os autores de arquivos. msi e não tem nenhum efeito sobre Windows Installer usuários. Os desenvolvedores podem querer remover esse espaço de armazenamento desperdiçado antes de enviar seu arquivo. msi final.

Para remover o espaço de armazenamento desperdiçado e reduzir o tamanho final dos arquivos. msi, você tem as seguintes opções.

-   Exporte todas as tabelas no banco de dados para arquivos. IDT e, em seguida, importe-as para um novo banco de dados. Isso produz o armazenamento mais compacto possível.
-   Use um utilitário de software para compactar o espaço de armazenamento de arquivos de documento OLE.

 

 



