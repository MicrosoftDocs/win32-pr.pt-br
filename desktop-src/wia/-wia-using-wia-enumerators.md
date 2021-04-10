---
description: O WIA fornece várias interfaces para enumerar vários recursos, propriedades e informações.
ms.assetid: d46d4c18-79cc-4f3c-9745-522ab2635068
title: Usando enumeradores WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ee42f99718cb36071b828e87e3a71de6d70ab5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164522"
---
# <a name="using-wia-enumerators"></a>Usando enumeradores WIA

O WIA fornece várias interfaces para enumerar vários recursos, propriedades e informações. As interfaces de enumeração de aquisição de imagem do Windows (WIA) são implementações específicas da interface de enumeração do COM (Standard Component Object Model). Para obter detalhes, consulte [IEnumXXXX](/previous-versions//ms680089(v=vs.85)).

A tabela a seguir fornece informações sobre as interfaces de enumeração WIA. 

| Interface                                                   | Como obter um ponteiro                                                                                                                                                                                    | Usadas para                                                                                                                             |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)       | Chame um método [**IWiaItem:: EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) ou [**IWiaItem2:: EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) de um item raiz WIA. | Enumera os recursos de um dispositivo de hardware WIA, como comandos de dispositivo e eventos.                                            |
| [**\_Informações de desenvolvimento do IEnumWIA \_**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)       | Chame o método [**IWiaDevMgr:: EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) ou [**IWiaDevMgr2:: EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md) .                                            | Enumera os dispositivos WIA disponíveis e fornece ponteiros para suas interfaces [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) . |
| [**\_Informações do formato IEnumWIA \_**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) | Chamar um método [**\_ \_ info de formato IWiaDataTransfer:: idtEnumWIA**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtenumwia_format_info) de um item.                                                                              | Enumera todas as informações de formato de imagem que um item WIA fornece.                                                                    |
| [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem)                   | Chamar um método [**IWiaItem:: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) ou [**IWiaItem2:: ENUMCHILDITEMS**](-wia-iwiaitem2-enumchilditems.md) do item WIA.                                          | Enumera os itens filho de um item WIA que representa um dispositivo ou uma pasta.                                                |



 

 

 
