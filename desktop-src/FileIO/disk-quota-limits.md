---
description: Descreve dois tipos de limites de cota de disco e como os limites de cota de disco são medidos.
ms.assetid: 6595d5e0-eb97-437e-abd2-3a04faefde7d
title: Limites de cota de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f51fff88bcb29d12c52387267c5e910ba36fa15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757559"
---
# <a name="disk-quota-limits"></a>Limites de cota de disco

O espaço em disco usado por cada arquivo é cobrado diretamente para o usuário que possui o arquivo. O proprietário de um arquivo é identificado pelo SID (identificador de segurança) nas informações de segurança do arquivo. O espaço total em disco cobrado para um usuário é a soma do comprimento de todos os fluxos de dados. Em outras palavras, os fluxos de conjunto de propriedades e os fluxos de dados de usuários residentes afetam a cota do usuário.

A cota não é cobrada por pontos de reanálise, descritores de segurança ou outros metadados associados aos arquivos. A compactação ou descompactação de arquivos não afeta o espaço em disco relatado para os arquivos. Portanto, as configurações de cota em um volume podem ser comparadas com as configurações em outro volume.

Há dois tipos de limites de cota de disco, conforme mostrado na tabela a seguir.



| Limite                        | Descrição                                                                                                                                                                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Limite de aviso<br/> | Você pode configurar o sistema para gerar uma entrada de arquivo de log do sistema quando o espaço em disco cobrado para o usuário exceder esse valor.<br/>                                                                                                                                         |
| Cota rígida<br/>        | Você pode configurar o sistema para gerar uma entrada de arquivo de log do sistema quando o espaço em disco cobrado para o usuário exceder esse valor. Você também pode configurar o sistema para negar espaço em disco adicional ao usuário quando o espaço em disco cobrado para o usuário exceder esse valor.<br/> |



 

O sistema de arquivos NTFS cria automaticamente uma entrada de cota de usuário quando um usuário grava pela primeira vez no volume. As entradas que são criadas automaticamente são atribuídas ao limite de aviso padrão e aos valores de limite de cota rígido para o volume.

 

 




