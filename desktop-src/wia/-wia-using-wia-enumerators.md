---
description: O WIA fornece várias interfaces para enumerar vários recursos, propriedades e informações.
ms.assetid: d46d4c18-79cc-4f3c-9745-522ab2635068
title: Usando enumeradores WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47b6e822d38c73171767d43afd416d09648bd6b82095b9408e2f17827751b0cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813466"
---
# <a name="using-wia-enumerators"></a>Usando enumeradores WIA

O WIA fornece várias interfaces para enumerar vários recursos, propriedades e informações. As interfaces Windows de enumeração WIA (Aquisição de Imagem) são todas implementações específicas da interface de enumeração PADRÃO Component Object Model (COM). Para obter detalhes, [consulte IEnumXXXX](/previous-versions//ms680089(v=vs.85)).

A tabela a seguir fornece informações sobre as interfaces de enumeração wia. 

| Interface                                                   | Como obter um ponteiro                                                                                                                                                                                    | Usadas para                                                                                                                             |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWIA \_ DEV \_ CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)       | Chame um [**método IWiaItem::EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) ou [**IWiaItem2::EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) de um item raiz WIA. | Enumera os recursos de um dispositivo de hardware WIA, como comandos e eventos do dispositivo.                                            |
| [**IEnumWIA \_ DEV \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)       | Chame o [**método IWiaDevMgr::EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) ou [**IWiaDevMgr2::EnumDeviceInfo.**](-wia-iwiadevmgr2-enumdeviceinfo.md)                                            | Enumera dispositivos WIA disponíveis e fornece ponteiros para suas interfaces [**IWiaPropertyStorage.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) |
| [**INFORMAÇÕES DE FORMATO IEnumWIA \_ \_**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) | Chame um [**método IWiaDataTransfer::idtEnumWIA \_ FORMAT \_ INFO**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtenumwia_format_info) de um item.                                                                              | Enumera todas as informações de formato de imagem que um item WIA fornece.                                                                    |
| [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem)                   | Chame um [**método IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) [**ou IWiaItem2::EnumChildItems**](-wia-iwiaitem2-enumchilditems.md) do item WIA.                                          | Enumera os itens filho de um item WIA que representa um dispositivo ou uma pasta.                                                |



 

 

 
