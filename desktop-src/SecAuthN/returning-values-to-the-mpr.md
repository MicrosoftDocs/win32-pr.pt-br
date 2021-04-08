---
description: As funções de rede do Windows retornam o \_ sucesso do WN em caso de êxito ou retornarão um valor diferente de zero, caso a função encontre um erro. Além disso, eles retornam informações de erro estendidas usando WNetSetLastError e SetLastError.
ms.assetid: cb9d29a1-b3a5-4440-a069-3cd1565b1699
title: Retornando valores para o MPR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c96a5636f57d5c926af4e43e676f0b6db75d164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921620"
---
# <a name="returning-values-to-the-mpr"></a>Retornando valores para o MPR

As funções de rede do Windows retornam o \_ sucesso do WN em caso de êxito ou retornarão um valor diferente de zero, caso a função encontre um erro. Além disso, eles retornam informações de erro estendidas usando [**WNetSetLastError**](/windows/desktop/api/Npapi/nf-npapi-wnetsetlasterrora) e [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror).

Para dar suporte ao comportamento acima, as funções de provedor de rede não devem chamar [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror) antes de retornar. Isso ocorre porque o MPR chama **SetLastError** para as funções na API do provedor de rede depois que elas retornam. Se os provedores de rede chamarem **SetLastError** diretamente, eles estarão fazendo chamadas de função redundantes. As funções de provedor de rede devem simplesmente retornar um código de erro. Os códigos de erro são especificados na descrição da função ou [valores de retorno](network-security-return-values.md). Além disso, as funções de provedor de rede podem retornar qualquer [código de erro do sistema](../debug/system-error-codes.md), como memória insuficiente. A única exceção é [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps), que deve retornar uma máscara que indica as funções com suporte pelo provedor de rede.

Se uma função de provedor de rede precisar retornar informações de erro estendidas, ela deverá chamar [**WNetSetLastError**](/windows/desktop/api/Npapi/nf-npapi-wnetsetlasterrora). Essa função é fornecida pelo sistema operacional Windows para uso por provedores de rede. Quando o provedor chama **WNetSetLastError**, ele pode definir uma cadeia de caracteres contendo informações adicionais sobre o erro. Essas informações são armazenadas por thread. Isso é análogo ao [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror) para aplicativos do Windows. O sistema operacional Windows chama **WNetSetLastError** para verificar se há uma cadeia de caracteres armazenada usando **WNetSetLastError** e, se encontrada, retorna as informações de erro estendidas para o aplicativo de chamada que iniciou a solicitação de rede.

> [!Note]  
> O prefixo WNet de [**WNetSetLastError**](/windows/desktop/api/Npapi/nf-npapi-wnetsetlasterrora) é enganoso, pois essa API, ao contrário de **WNetSetLastError**, não faz parte do conjunto de API de rede do Windows. **WNetSetLastError** destina-se ao uso somente por provedores de rede. O nome, **WNetSetLastError**, é retido para compatibilidade com os provedores existentes.

 

 

 
