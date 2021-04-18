---
description: Os objetos de arquivo funcionam como a interface lógica entre os processos de kernel e de modo de usuário e os dados de arquivo que residem no disco físico.
ms.assetid: 53aabb35-4601-42d1-ac73-385473ff91e2
title: Objetos de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e37793ad6c31ac86809047a3ec0d34afc3efc34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753481"
---
# <a name="file-objects"></a>Objetos de arquivo

Os *objetos de arquivo* funcionam como a interface lógica entre os processos de kernel e de modo de usuário e os dados de arquivo que residem no disco físico. Um objeto File contém ambos os dados gravados no arquivo e o seguinte conjunto de atributos mantidos pelo kernel.



| Tipo de informação                                              | Finalidade                                                                                                                                                                                         |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome do arquivo                                                     | Nomeia o arquivo físico correspondente.                                                                                                                                                          |
| Deslocamento de byte atual                                           | Usado em e/s de arquivo síncrono (descrito posteriormente nesta seção) para identificar o local inicial atual das operações de leitura e gravação.                                                          |
| Modo de compartilhamento                                                    | Especifica se um segundo processo pode abrir um arquivo para acesso de leitura, gravação ou exclusão enquanto o processo inicial ainda está acessando-o.                                                           |
| Modo de e/s                                                      | Especifica se o processo inicial abriu o arquivo para e [/s síncrona](synchronous-and-asynchronous-i-o.md), em cache ou não armazenada em cache, e/s sequencial ou aleatória, e assim por diante. |
| Ponteiro para objeto de dispositivo                                      | Identifica o dispositivo físico no qual os dados de arquivo residem.                                                                                                                                        |
| Ponteiro para o bloco de parâmetro de volume ou o [ **VPB**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_vpb) | Identifica o volume ou a partição em que os dados de arquivo residem.                                                                                                                                    |
| Ponteiro para ponteiros de objeto de seção                            | Identifica uma estrutura raiz que descreve um [arquivo mapeado](/windows/desktop/Memory/file-mapping).                                                                                                                  |
| Ponteiro para o mapa de cache privado                                  | Identifica os dados de arquivo que estão armazenados em cache no momento.                                                                                                                                              |



 

Esses atributos são definidos como parte da estrutura [**do \_ objeto de arquivo**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) em Ntddk. h. Consulte a definição dessa estrutura na documentação do Windows Driver Kit (WDK) para obter os tamanhos de dados e os tipos de valores.

 

 
