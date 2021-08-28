---
description: Os qualificadores a seguir são usados pelo provedor WDM em arquivos de driver de dispositivo MOF quando estão extraindo dados do WNODEs para gerar instâncias de classes de driver WDM.
ms.assetid: 11b0af59-979f-4908-baef-c9ec564b3cfd
ms.tgt_platform: multiple
title: Qualificadores específicos para o provedor WDM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: 673b53d8cea23cd044175129af85c367f6f20c8dc92240c8bdf52f34708d96f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996076"
---
# <a name="qualifiers-specific-to-the-wdm-provider"></a>Qualificadores específicos para o provedor WDM

Os qualificadores a seguir são usados pelo [provedor WDM](/windows/desktop/WmiCoreProv/wdm-provider) em arquivos de driver de dispositivo MOF quando estão extraindo dados do WNODEs para gerar instâncias de classes de driver WDM.

<dt>

<span id="MissingValue"></span><span id="missingvalue"></span><span id="MISSINGVALUE"></span>**Faltandovalue**
</dt> <dd>

Tipo de dados: **DWORD, array, uint8, UInt16, UInt32, sint8, sint16 ou sint32.**

Aplica-se a: Propriedades

Um valor ausente para essa propriedade deve ser representado por **NULL** em vez de 0 (zero).

</dd> <dt>

<span id="WMIDataId"></span><span id="wmidataid"></span><span id="WMIDATAID"></span>**WMIDataId**
</dt> <dd>

Tipo de dados: **UInt32**

Aplica-se a: Propriedades

Índice na WNODE dos dados da propriedade. O provedor WDM usa esse qualificador para determinar como os dados são formatados ao extrair dados do WNODE e gerar classes WMI. O valor inicial é 1.

</dd> <dt>

<span id="WMIExpense"></span><span id="wmiexpense"></span><span id="WMIEXPENSE"></span>**WMIExpense**
</dt> <dd>

Tipo de dados: **UInt32**

Aplica-se a: classes

Indicação do custo do recurso para acessar o bloco de dados. Por exemplo, as informações de geometria de disco não exigem muitos recursos para obter, pois estão disponíveis na extensão do dispositivo. O desempenho de leitura/gravação de disco é mais intensivo por recursos porque requer trabalho extra em cada operação de leitura/gravação. Portanto, o valor do qualificador **WMIExpense** é maior para o desempenho de leitura/gravação no disco.

</dd> <dt>

<span id="WMIMethodId"></span><span id="wmimethodid"></span><span id="WMIMETHODID"></span>**WMIMethodId**
</dt> <dd>

Tipo de dados: **UInt32**

Aplica-se a: métodos

Índice na WNODE dos dados da propriedade. O provedor WDM usa esse qualificador para determinar como os dados são formatados ao extrair dados do WNODE e gerar classes WMI. O valor inicial é 1.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



 

