---
title: Referência de funções de suporte
description: As funções a seguir são fornecidas para protocolos de roteamento pelo Gerenciador de roteador.
ms.assetid: 4e88c9fe-f6ec-4f9c-88b1-8726e10d0f6d
keywords:
- Interface do protocolo de roteamento RRAS, funções de suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fa2af1b38e88e9f3b7a55e8026ad42f4b1d0cff26de3798fb04621a1288ad9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073706"
---
# <a name="support-functions-reference"></a>Referência de funções de suporte

As funções a seguir são fornecidas para protocolos de roteamento pelo Gerenciador de roteador. Quando o Gerenciador de roteador chama a função [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) (implementada pelo protocolo de roteamento), o Gerenciador de roteador passa o protocolo de roteamento a uma estrutura de [**\_ funções de suporte**](/windows/desktop/api/Routprot/ns-routprot-support_functions_50) que contém ponteiros para essas funções:

[**DemandDialRequest**](/previous-versions/windows/desktop/legacy/aa373924(v=vs.85))

[**MIBEntryCreate**](/previous-versions/windows/desktop/legacy/aa374538(v=vs.85))

[**MIBEntryDelete**](/previous-versions/windows/desktop/legacy/aa374539(v=vs.85))

[**MIBEntryGet**](/previous-versions/windows/desktop/legacy/aa374540(v=vs.85))

[**MIBEntryGetFirst**](/previous-versions/windows/desktop/legacy/aa374541(v=vs.85))

[**MIBEntryGetNext**](/previous-versions/windows/desktop/legacy/aa374542(v=vs.85))

[**MIBEntrySet**](/previous-versions/windows/desktop/legacy/aa374543(v=vs.85))

[**SetInterfaceReceiveType**](/previous-versions/windows/desktop/legacy/aa382181(v=vs.85))

[**ValidateRoute**](/previous-versions/windows/desktop/legacy/aa382342(v=vs.85))

 

 