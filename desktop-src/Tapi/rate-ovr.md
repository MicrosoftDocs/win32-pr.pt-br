---
description: A taxa ou largura de banda de uma chamada especifica a velocidade da transmissão de dados. Três pontos de dados identificam a taxa atual, a taxa máxima para um modo de portador especificado e a taxa mínima para o modo de portador.
ms.assetid: bc373ac5-a986-483f-a136-60cdc2e2c6b0
title: Tarifa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce0af0b2dd6dfe34759753f52773bafe0bdf2bf8f4472ed863dcc6c8b0f10a0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060554"
---
# <a name="rate"></a>Tarifa

A taxa (ou largura de banda) de uma chamada especifica a velocidade da transmissão de dados. Três pontos de dados identificam a taxa: a taxa atual, a taxa máxima para um modo de portador especificado e a taxa mínima para o modo de portador.

Nem todos os provedores de serviços suportam o uso dessas informações.

**TAPI 2.x: **[**lineSetCallParams,**](/windows/win32/api/tapi/nf-tapi-linesetcallparams) [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwMinRate** ou **dwMaxRate** membro [**de LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

**TAPI 3.x: **[**ITCallInfo::get \_ CallInfoLong,**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) [**ITCallInfo::p ut \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL \_ MAXRATE,** **CIL \_ MINRATE** ou **membro CIL \_ RATE** de [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)

**TSPI: **[**mensagem \_ LINE CALLINFO,**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) com *dwParam1* definido como LINECALLINFOSTATE \_ RATE

 

 
