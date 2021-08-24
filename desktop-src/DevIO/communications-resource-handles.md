---
description: Um processo usa a função CreateFile para abrir um identificador para um recurso de comunicação.
ms.assetid: eaef6067-97a6-40c4-84ec-c0d86af6bb4a
title: Identificadores de recursos de comunicação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 585d7ab257c36bc288a494c2e55d9f192749e9742b0eb88ead6d0b0ffad919cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768756"
---
# <a name="communications-resource-handles"></a>Identificadores de recursos de comunicação

Um processo usa a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir um identificador para um recurso de comunicação. Por exemplo, a especificação de COM1 abre um identificador para uma porta serial e a LPT1 abre um identificador para uma porta paralela. Se o recurso especificado estiver sendo usado atualmente por outro processo, **CreateFile** falhará. Qualquer thread do processo pode usar o identificador retornado por **CreateFile** para identificar o recurso em qualquer uma das funções que acessam o recurso.

Quando o processo chama [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir um recurso de comunicação, ele especifica os seguintes atributos:

-   Que tipo de acesso de leitura/gravação existe para o recurso especificado.
-   Se o identificador pode ser herdado por processos filho.
-   Se o identificador pode ser usado em operações de e/s sobrepostas (assíncronas). (Para obter uma descrição das operações sobrepostas, consulte [sincronização](/windows/desktop/Sync/synchronization).)

Quando o processo usa [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir um recurso de comunicação, ele deve especificar determinados valores para os seguintes parâmetros:

-   O parâmetro *fdwShareMode* deve ser zero, abrindo o recurso para acesso exclusivo.
-   O parâmetro *fdwCreate* deve especificar o \_ sinalizador Open existing.
-   O parâmetro *hTemplateFile* deve ser **nulo**.

Ao usar [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir um identificador diretamente em um dispositivo, um aplicativo deve usar os caracteres especiais " \\ \\ . \\ " para identificar o dispositivo. Por exemplo, para abrir um identificador para a unidade A, especifique \\ \\ . \\ r: para o parâmetro *lpszName* de **CreateFile**. O processo de chamada pode usar o identificador na função [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) para enviar códigos de controle para o dispositivo.

 

 
