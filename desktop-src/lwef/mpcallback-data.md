---
title: Estrutura de MPCALLBACK_DATA (MpClient. h)
description: Dados passados para a função de retorno de chamada.
ms.assetid: EA8E6C1E-F80B-4247-B073-C78D49A354CF
keywords:
- recursos de ambiente de Windows herdado da estrutura de MPCALLBACK_DATA
- Windows recursos de ambiente herdados do ponteiro de estrutura do PMPCALLBACK_DATA
topic_type:
- apiref
api_name:
- MPCALLBACK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1eb129101c341485a1e6b5763a0325cbf586a6e51e5e2875b4465696c39df8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883648"
---
# <a name="mpcallback_data-structure"></a>\_Estrutura de dados MPCALLBACK

Dados passados para a função de retorno de chamada.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPCALLBACK_DATA {
  MPNOTIFY        Notify;
  HRESULT         hResult;
  ULARGE_INTEGER  TimeStamp;
  MPCALLBACK_TYPE Type;
  union {
    PMPSTATUS_DATA         pStatusData;
    PMPSCAN_DATA           pScanData;
    PMPCLEAN_DATA          pCleanData;
    PMPCLEAN_PRECHECK_DATA pPrecheckData;
    PMPTHREAT_DATA         pThreatData;
    PMPSIGUPDATE_DATA      pSigUpdateData;
    PMPSAMPLE_DATA         pSampleData;
    PMPRESERVED_DATA       pReservedData;
    PMPCONFIGURATION_DATA  pConfigurationData;
    PMPFASTPATH_DATA       pFastPathData;
    PMPEXPIRATION_DATA     pExpirationData;
    PMPNIS_PRIVATE_DATA    pNISPrivateData;
    PMPHEALTH_DATA         pHealthData;
    PMPENDOFLIFE_DATA      pEndOfLifeData;
    PMPMALWARETOAST_DATA   pMalwareToastData;
  } Data;
} MPCALLBACK_DATA, *PMPCALLBACK_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**Notificar**
</dt> <dd>

Tipo: **[ **mpnotify**](mpnotify.md)**

</dd> <dd>

Notificação de alteração para o relatório.

</dd> <dt>

**Resultado**
</dt> <dd>

Tipo: **HRESULT**

</dd> <dd>

Código de erro, no caso de uma falha interna.

</dd> <dt>

**Estampa**
</dt> <dd>

Tipo: **ULARGE \_ inteiro**

</dd> <dd>

Carimbo de data/hora atual.

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **\_ tipo de MPCALLBACK**](mpcallback-type.md)**

</dd> <dd>

Tipo de dados especial de retorno de chamada.

</dd> <dt>

**Dados**
</dt> <dd>

Dados especiais de retorno de chamada. O ponteiro para a estrutura apropriada depende do valor do **tipo**.

<dl> <dt>

**pStatusData**
</dt> <dd>

Tipo: **\_ dados de PMPSTATUS**

</dd> <dd>

Ao **digitar** o  ==  **\_ status de MPCALLBACK**. Consulte [**\_ dados do MPSTATUS**](mpstatus-data.md).

</dd> <dt>

**pScanData**
</dt> <dd>

Tipo: **\_ dados de PMPSCAN**

</dd> <dd>

Quando o **tipo**  ==  **MPCALLBACK \_ Scan**. Consulte [**\_ dados do MPSCAN**](mpscan-data.md).

</dd> <dt>

**pCleanData**
</dt> <dd>

Tipo: **\_ dados de PMPCLEAN**

</dd> <dd>

Quando **digite**  ==  **MPCALLBACK \_ Clean**. Consulte [**\_ dados do MPCLEAN**](mpclean-data.md).

</dd> <dt>

**pPrecheckData**
</dt> <dd>

Tipo: **PMPCLEAN \_ \_ dados de verificação**

</dd> <dd>

Quando MPCALLBACK, **digite**  ==  **\_ precheck**. Consulte [**MPCLEAN \_ precheck \_ Data**](mpclean-precheck-data.md).

</dd> <dt>

**pThreatData**
</dt> <dd>

Tipo: **\_ dados de PMPTHREAT**

</dd> <dd>

Quando **digitar**  ==  **\_ ameaça MPCALLBACK**. Consulte [**\_ dados do MPTHREAT**](mpthreat-data.md).

</dd> <dt>

**pSigUpdateData**
</dt> <dd>

Tipo: **\_ dados de PMPSIGUPDATE**

</dd> <dd>

Quando **digite**  ==  **MPCALLBACK \_ SIGUPDATE**. Consulte [**\_ dados do MPSIGUPDATE**](mpsigupdate-data.md).

</dd> <dt>

**pSampleData**
</dt> <dd>

Tipo: **\_ dados de PMPSAMPLE**

</dd> <dd>

Ao **digitar** o  ==  **\_ exemplo MPCALLBACK**. Consulte [**\_ dados do MPSAMPLE**](mpsample-data.md).

</dd> <dt>

**pReservedData**
</dt> <dd>

Tipo: **\_ dados de PMPRESERVED**

</dd> <dd>

Quando o **tipo**  ==  **MPCALLBACK \_ reservado**. Consulte [**\_ dados do MPRESERVED**](mpreserved-data.md).

</dd> <dt>

**pConfigurationData**
</dt> <dd>

Tipo: **\_ dados de PMPCONFIGURATION**

</dd> <dd>

Quando **tipo** de  ==  **\_ \_ notificação de configuração MPCALLBACK**. Consulte [**\_ dados do MPCONFIGURATION**](mpconfiguration-data.md).

</dd> <dt>

**pFastPathData**
</dt> <dd>

Tipo: **\_ dados de PMPFASTPATH**

</dd> <dd>

Quando **digite**  ==  **MPCALLBACK \_ FASTPATH**. Consulte [**\_ dados do MPFASTPATH**](mpfastpath-data.md).

</dd> <dt>

**pExpirationData**
</dt> <dd>

Tipo: **\_ dados de PMPEXPIRATION**

</dd> <dd>

Quando **tipo**  ==  **MPCALLBACK \_ \_ expiração do produto**. Consulte [**\_ dados do MPEXPIRATION**](mpexpiration-data.md).

</dd> <dt>

**pNISPrivateData**
</dt> <dd>

Tipo: **PMPNIS \_ Private \_ Data**

</dd> <dd>

Quando o **tipo**  ==  **MPCALLBACK \_ NIS \_ privado**. Consulte [**MPNIS \_ Private \_ Data**](mpnis-private-data.md).

</dd> <dt>

**pHealthData**
</dt> <dd>

Tipo: **\_ dados de PMPHEALTH**

</dd> <dd>

Ao **digitar**  ==  **MPCALLBACK \_ Health**. Consulte [**\_ dados do MPHEALTH**](mphealth-data.md).

</dd> <dt>

**pEndOfLifeData**
</dt> <dd>

Tipo: **\_ dados de PMPENDOFLIFE**

</dd> <dd>

Quando **digite**  ==  **MPCALLBACK \_ ENDOFLIFE**. Consulte [**\_ dados do MPENDOFLIFE**](mpendoflife-data.md).

</dd> <dt>

**pMalwareToastData**
</dt> <dd>

Tipo: **\_ dados de PMPMALWARETOAST**

</dd> <dd>

Quando **digite**  ==  **MPCALLBACK \_ MALWARETOAST**. Consulte [**\_ dados do MPMALWARETOAST**](mpmalwaretoast-data.md).

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**tipo de MPCALLBACK \_**](mpcallback-type.md)
</dt> <dt>

[**dados do MPCLEAN \_**](mpclean-data.md)
</dt> <dt>

[**MPCLEAN \_ dados de verificação \_**](mpclean-precheck-data.md)
</dt> <dt>

[**dados do MPCONFIGURATION \_**](mpconfiguration-data.md)
</dt> <dt>

[**dados do MPENDOFLIFE \_**](mpendoflife-data.md)
</dt> <dt>

[**dados do MPEXPIRATION \_**](mpexpiration-data.md)
</dt> <dt>

[**dados do MPFASTPATH \_**](mpfastpath-data.md)
</dt> <dt>

[**dados do MPHEALTH \_**](mphealth-data.md)
</dt> <dt>

[**dados do MPMALWARETOAST \_**](mpmalwaretoast-data.md)
</dt> <dt>

[**MPNIS \_ \_ dados privados**](mpnis-private-data.md)
</dt> <dt>

[**MPNOTIFY**](mpnotify.md)
</dt> <dt>

[**dados do MPRESERVED \_**](mpreserved-data.md)
</dt> <dt>

[**dados do MPSAMPLE \_**](mpsample-data.md)
</dt> <dt>

[**dados do MPSCAN \_**](mpscan-data.md)
</dt> <dt>

[**dados do MPSIGUPDATE \_**](mpsigupdate-data.md)
</dt> <dt>

[**dados do MPSTATUS \_**](mpstatus-data.md)
</dt> <dt>

[**dados do MPTHREAT \_**](mpthreat-data.md)
</dt> </dl>

 

 





