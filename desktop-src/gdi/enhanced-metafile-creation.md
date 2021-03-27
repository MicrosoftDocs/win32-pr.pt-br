---
description: Você cria um metarquivo avançado usando a função CreateEnhMetaFile, fornecendo os argumentos apropriados.
ms.assetid: b012e50e-a7f5-4687-9833-38dacc113d77
title: Criação de metarquivo aprimorada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 080c350e41e895c5d4bf834a6f407cca5907743d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661610"
---
# <a name="enhanced-metafile-creation"></a>Criação de metarquivo aprimorada

Você cria um metarquivo avançado usando a função [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) , fornecendo os argumentos apropriados. O sistema usa esses argumentos para manter dimensões de imagem, determinar se o metarquivo deve ser armazenado em um disco ou na memória e assim por diante.

Para manter as dimensões de imagem nos dispositivos de saída, o [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) requer a resolução do dispositivo de referência. Esse *dispositivo de referência* é o dispositivo no qual a imagem apareceu pela primeira vez e o *controlador de domínio de referência* é o contexto do *dispositivo* associado ao dispositivo de referência. Ao chamar a função **CreateEnhMetaFile** , você deve fornecer um identificador que identifique esse DC. Você pode obter esse identificador chamando a função [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) ou [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) . Você também pode especificar **NULL** como o identificador para usar o dispositivo de vídeo atual para o dispositivo de referência.

A maioria dos aplicativos armazena imagens permanentemente e, portanto, cria um metarquivo avançado que é armazenado em um disco; no entanto, há algumas instâncias quando isso não é necessário. Por exemplo, um aplicativo de processamento de texto que fornece recursos de desenho de gráfico pode armazenar um gráfico definido pelo usuário na memória como um metarquivo avançado e, em seguida, copiar os bits de metarquivo aprimorados da memória para o arquivo de documento do usuário. Um aplicativo que requer um metarquivo que é armazenado permanentemente em um disco deve fornecer o nome do arquivo quando ele chama [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea). Se você não fornecer um nome de arquivo, o sistema tratará automaticamente o metarquivo como um arquivo temporário e o armazenará na memória.

Você pode adicionar uma descrição de texto opcional a um metarquivo que contém informações sobre a imagem e o autor. Um aplicativo pode exibir essas cadeias de caracteres na caixa de diálogo abrir arquivo para fornecer ao usuário informações sobre o conteúdo do metarquivo que ajudarão na seleção do arquivo apropriado. Se um aplicativo incluir a descrição do texto, ele deverá fornecer um ponteiro para a cadeia de caracteres quando ele chamar [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea).

Quando o [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) é executado com sucesso, ele retorna um identificador que identifica um contexto de dispositivo de metarquivo especial. Um contexto de dispositivo de metarquivo é exclusivo, pois ele está associado a um arquivo em vez de a um dispositivo de saída. Quando o sistema processa uma função GDI que recebeu um identificador para um contexto de dispositivo de metarquivo, ele converte a função GDI em um registro de metarquivo avançado e anexa o registro ao final do metarquivo avançado.

Depois que uma imagem é concluída e o último registro é anexado ao metarquivo avançado, o aplicativo pode fechar o arquivo chamando a função [**CloseEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-closeenhmetafile) . Essa função fecha e exclui o contexto de dispositivo de metarquivo especial e retorna um identificador que identifica o metarquivo avançado.

Para excluir um metarquivo de formato avançado ou um identificador de metarquivo de formato avançado, chame a função [**DeleteEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-deleteenhmetafile) .

 

 



