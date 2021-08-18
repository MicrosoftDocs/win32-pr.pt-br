---
title: Funções de palavras-chave dinâmicas do firewall
description: As palavras-chave dinâmicas do firewall contêm as funções a seguir.
keywords:
- Palavras-chave dinâmicas do firewall, funções
ms.topic: article
ms.date: 05/13/2021
ms.localizationpriority: low
ms.openlocfilehash: 1aacc30ecac9cddca5f986878da1ff633660152144e8ca2fe1440fdecfd61e3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015646"
---
# <a name="firewall-dynamic-keywords-functions"></a>Funções de palavras-chave dinâmicas do firewall

As palavras-chave dinâmicas do firewall contêm as funções a seguir.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) | Solicita a entrega de notificações sobre alterações em objetos específicos de endereço de[palavra-chave](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)dinâmico (FW_DYNAMIC_KEYWORD_ADDRESS0 ). |
| [**FwpmDynamicKeywordUnsubscribe0**](/windows/win32/api/fwpmu/FwpmDynamicKeywordUnsubscribe0) | Cancela a entrega de notificações relacionadas a alterações em objetos de endereço de[palavra-chave](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)dinâmico específico ( FW_DYNAMIC_KEYWORD_ADDRESS0 ). |
| [**PFN_FWADDDYNAMICKEYWORDADDRESS0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) | Tipo de ponteiro de função do ponto de entrada no serviço que você chama para adicionar o endereço de palavra-chave dinâmico especificado. |
| [**PFN_FWDELETEDYNAMICKEYWORDADDRESS0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0) | Tipo de ponteiro de função do ponto de entrada no serviço que você chama para excluir o endereço de palavra-chave dinâmico com a ID especificada. |
| [**PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) | Tipo de ponteiro de função do ponto de entrada no serviço que você chama para enumerar os endereços de palavra-chave dinâmicos específicos por ID. |
| [**PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) | Tipo de ponteiro de função do ponto de entrada no serviço que você chama para enumerar endereços de palavra-chave dinâmicos por tipo. Você pode solicitar um subconjunto específico de objetos com base nos sinalizadores de enumeração passados. |
| [**PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) | Tipo de ponteiro de função do ponto de entrada no serviço que você chama para liberar structs de dados de endereço dinâmico de palavra-chave alocados pelo serviço. |
| [**PFN_FWUPDATEDYNAMICKEYWORDADDRESS0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0) | Tipo de ponteiro de função do ponto de entrada no serviço que você chama para atualizar o endereço de palavra-chave dinâmico com a ID de entrada. |

## <a name="related-topics"></a>Tópicos relacionados

* [Referência de palavras-chave dinâmicas do firewall](firewall-dynamic-keywords-reference.md)
