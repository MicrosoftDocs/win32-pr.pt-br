---
title: Enumeração DODownloadPropertyEx
description: Especifica a ID das propriedades estendidas para a operação de download.
keywords:
- Enumeração DODownloadPropertyEx, DODownloadPropertyEx
topic_type:
- apiref
api_name:
- DODownloadPropertyEx
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: f5ec26d845fd6df2bfe0e84fffed0979c39e1971244788c9dfe5ddd3a0c0beca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990376"
---
# <a name="dodownloadpropertyex-enumeration"></a>Enumeração DODownloadPropertyEx

> [!IMPORTANT]
> A enumeração **DODownloadPropertyEx** foi preterida. Em vez disso, use a enumeração [Dobaixeproperty](../deliveryoptimizationdownloadtypes/ne-deliveryoptimizationdownloadtypes-dodownloadproperty.md) com [IDODownload:: GetProperty](../do/nf-do-idodownload-getproperty.md) e [IDODownload:: SetProperty](../do/nf-do-idodownload-setproperty.md).

A enumeração **DODownloadPropertyEx** especifica a ID das propriedades estendidas para a operação fazer download. Essa enumeração é usada pela interface **IDODownloadInternal** e um valor **Variant** é usado para obter e definir o valor da propriedade.

## <a name="syntax"></a>Syntax

```cpp
typedef enum _DODownloadPropertyEx
{
  DODownloadPropertyEx_UpdateId = 0,
  DODownloadPropertyEx_CorrelationVector,
  DODownloadPropertyEx_DecryptionInfo,    
  DODownloadPropertyEx_IntegrityCheckInfo,   
  DODownloadPropertyEx_IntegrityCheckMandatory, 
  DODownloadPropertyEx_TotalSizeBytes, 
  DODownloadPropertyEx_TempLocalFileUsage 
} DODownloadPropertyEx;
```
## <a name="constants"></a>Constantes

| Requisito | Valor |
|-|-|
| DODownloadPropertyEx_UpdateId | Reservado. Não use. |
| DODownloadPropertyEx_CorrelationVector | Opcional. Define um vetor de correlação específico para fins de telemetria. O tipo de variante é VT_BSTR. |
| DODownloadPropertyEx_DecryptionInfo | Reservado. Não use. |
| DODownloadPropertyEx_IntegrityCheckInfo | Opcional somente gravação. Define o local do arquivo de hash da parte (PHF), que é usado pelo para executar verificações de integridade de tempo de execução no conteúdo baixado. O tipo de variante é VT_BSTR. |
| DODownloadPropertyEx_IntegrityCheckMandatory | Opcional. Define um sinalizador booliano que indica se o uso do arquivo de hash da parte (PHF) é obrigatório. Se VARIANT_TRUE, o download será anulado quando a verificação de integridade falhar. O tipo de variante é VT_BOOL. |
| DODownloadPropertyEx_TotalSizeBytes | Reservado. Não use. |
| DODownloadPropertyEx_TempLocalFileUsage | Reservado. Não use. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | Windows 10, versão 1809 \[ Somente aplicativos Win32\] |
| **Servidor mínimo com suporte** | Windows Somente aplicativos Win32 do servidor versão 1809 \[\] |
| **Cabeçalho** | DODownloadInternal. h |
