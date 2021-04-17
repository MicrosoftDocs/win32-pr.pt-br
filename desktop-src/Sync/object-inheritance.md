---
description: Ao criar um processo com a função CreateProcess, você pode especificar que o processo herde identificadores para mutex, evento, semáforo ou objetos de temporizador usando a \_ estrutura atributos de segurança.
ms.assetid: 36491a5c-7599-4f69-ab76-d3a62261a151
title: Herança de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6087ae3699e7628ab97871ede41cc2e406e40157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755537"
---
# <a name="object-inheritance"></a>Herança de objetos

Ao criar um processo com a função [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) , você pode especificar que o processo herde identificadores para mutex, evento, semáforo ou objetos de temporizador usando a estrutura [**\_ atributos de segurança**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) . O identificador herdado pelo processo tem o mesmo acesso ao objeto que o identificador original. O identificador herdado aparece na tabela de identificadores do processo criado, mas você deve comunicar o valor do identificador para o processo criado. Você pode fazer isso especificando o valor como um argumento de linha de comando ao chamar **CreateProcess**. Em seguida, o processo criado usa a função [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) para recuperar a cadeia de caracteres de linha de comando e converter o argumento Handle em um identificador utilizável. Para obter mais informações, consulte [Herança](../procthread/inheritance.md).

 

 
