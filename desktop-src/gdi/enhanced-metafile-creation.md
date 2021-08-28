---
description: Você cria um metadado aprimorado usando a função CreateEnhMetaFile, fornecendo os argumentos apropriados.
ms.assetid: b012e50e-a7f5-4687-9833-38dacc113d77
title: Criação aprimorada de metadados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c89a4a05a18ecce4bc1b1fe3689e4f7a8dc64c833db4eac937da4f9a290dd3ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831986"
---
# <a name="enhanced-metafile-creation"></a>Criação aprimorada de metadados

Você cria um metadado aprimorado usando a [**função CreateEnhMetaFile,**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) fornecendo os argumentos apropriados. O sistema usa esses argumentos para manter dimensões de imagem, determinar se o metadado deve ser armazenado em um disco ou na memória e assim por diante.

Para manter dimensões de imagem entre dispositivos de saída, [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) requer a resolução do dispositivo de referência. Esse *dispositivo de referência* é o dispositivo no qual a  imagem apareceu pela primeira vez e o *DC* de referência é o contexto do dispositivo associado ao dispositivo de referência. Ao chamar a **função CreateEnhMetaFile,** você deve fornecer um identificador que identifique esse DC. Você pode obter esse handle chamando a [**função GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) [**ou CreateDC.**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) Você também pode especificar **NULL** como o alça para usar o dispositivo de exibição atual para o dispositivo de referência.

A maioria dos aplicativos armazena imagens permanentemente e, portanto, cria um metadado aprimorado armazenado em um disco; no entanto, há algumas instâncias quando isso não é necessário. Por exemplo, um aplicativo de processamento de palavras que fornece recursos de desenho de gráfico pode armazenar um gráfico definido pelo usuário na memória como um metadado aprimorado e copiar os bits de metadados aprimorados da memória para o arquivo de documento do usuário. Um aplicativo que requer um metadado armazenado permanentemente em um disco deve fornecer o nome do arquivo quando chama [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea). Se você não fornecer um nome de arquivo, o sistema tratará automaticamente o metadado como um arquivo temporário e o armazenará na memória.

Você pode adicionar uma descrição de texto opcional a um metadado que contém informações sobre a imagem e o autor. Um aplicativo pode exibir essas cadeias de caracteres na caixa de diálogo Arquivo Aberto para fornecer ao usuário informações sobre o conteúdo de metadados que ajudarão na seleção do arquivo apropriado. Se um aplicativo incluir a descrição de texto, ele deverá fornecer um ponteiro para a cadeia de caracteres quando chamar [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea).

Quando [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) é bem-sucedido, ele retorna um identificador que identifica um contexto de dispositivo de metadados especial. Um contexto de dispositivo de metadados é exclusivo, já que ele está associado a um arquivo em vez de a um dispositivo de saída. Quando o sistema processa uma função GDI que recebeu um handle em um contexto de dispositivo de metadados, ele converte a função GDI em um registro de metadados aprimorado e anexa o registro ao final do metadado aprimorado.

Depois que uma imagem for concluída e o último registro for anexado ao metadado aprimorado, o aplicativo poderá fechar o arquivo chamando a [**função CloseEnhMetaFile.**](/windows/desktop/api/Wingdi/nf-wingdi-closeenhmetafile) Essa função fecha e exclui o contexto especial do dispositivo de metarquivo e retorna um identificador que identifica o metarquivo aprimorado.

Para excluir um metarquivo de formato avançado ou um alça de metarquivo de formato avançado, chame a [**função DeleteEnhMetaFile.**](/windows/desktop/api/Wingdi/nf-wingdi-deleteenhmetafile)

 

 



