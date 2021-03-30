---
title: Registro de cliente de canal virtual
description: Você deve armazenar o nome da DLL do cliente no registro.
ms.assetid: bf84b2f4-55c2-45fd-bba7-8ff3efe4b1fd
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd7ecf128f125f6f25202bf683f8aa55ae4f257
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641248"
---
# <a name="virtual-channel-client-registration"></a>Registro de cliente de canal virtual

Você deve armazenar o nome da DLL do cliente no registro.

No registro, adicione uma subchave a um dos seguintes locais:

**HKEY \_ Software do \_ usuário atual** \\  \\  \\  \\  \\ **suplementos** do cliente Microsoft Terminal Server Client

**HKEY \_ \_** \\  \\ Suplementos de conexão de cliente **do Microsoft** \\ **Terminal Server Client** \\  \\  software atual

> [!Note]  
> No caminho do registro, a *conexão* representa o nome de uma conexão no Gerenciador de conexões.

 

As entradas na chave de **\\ \\ suplementos padrão** se aplicam a todas as conexões. As entradas na chave de **\\  \\ suplementos de conexão** aplicam-se somente à conexão identificada pela *conexão*. As conexões podem ser criadas e gerenciadas usando o Gerenciador de conexões.

A subchave pode receber qualquer nome. Ele deve conter um valor de reg **\_ sz** ou **reg \_ expande \_ sz** e pode, opcionalmente, conter um valor **reg \_ DWORD** . A sintaxe do valor **reg \_ sz** ou **reg \_ expande \_ sz** é a seguinte:

``` syntax
Name = DLLname
```

Se **Name** for um valor **reg \_ Expand \_ sz** , ele poderá conter variáveis de ambiente não expandidas que são expandidas no tempo de execução.

O valor de *DllName* pode ser um caminho totalmente qualificado. Se *DllName* não contiver um caminho, a estratégia de pesquisa padrão de dll será usada. Para obter mais informações, consulte a seção comentários para [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya).

 

 