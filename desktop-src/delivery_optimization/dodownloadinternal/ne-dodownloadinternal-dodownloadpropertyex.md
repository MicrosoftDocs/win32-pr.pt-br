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
ms.openlocfilehash: 5df0f53778d9059ef8767f5b8052940847e36c00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824480"
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
| **Cliente mínimo com suporte** | Somente aplicativos do Windows 10, versão 1809 \[ Win32\] |
| **Servidor mínimo com suporte** | Somente aplicativos do Windows Server, versão 1809 \[ Win32\] |
| **Cabeçalho** | DODownloadInternal. h |
