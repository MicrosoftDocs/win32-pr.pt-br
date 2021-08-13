---
title: Enumeração DODownloadProperty
description: Especifica a ID das propriedades para a operação de download do DO.
keywords:
- Enumeração DODownloadProperty, DODownloadProperty
topic_type:
- apiref
api_name:
- DODownloadProperty
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: 2e36dc783a7b2c7da23f4513f198b7871f97fe6576f60ffdd6f0fcbd7a11e3f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544568"
---
# <a name="dodownloadproperty-enumeration"></a>Enumeração DODownloadProperty

A **enumeração DODownloadProperty** especifica a ID das propriedades para a operação de download do DO. Essa enumeração é usada pela interface **IDODownload** e executada por um valor VARIANT, em que o tipo de valor está contido.

## <a name="syntax"></a>Sintaxe

```cpp
typedef enum _DODownloadProperty
{
  DODownloadProperty_Id = 0,
  DODownloadProperty_Uri,
  DODownloadProperty_ContentId,
  DODownloadProperty_DisplayName,
  DODownloadProperty_LocalPath,
  DODownloadProperty_HttpCustomHeaders,
  DODownloadProperty_CostPolicy,
  DODownloadProperty_SecurityFlags,
  DODownloadProperty_CallbackFreqPercent,
  DODownloadProperty_CallbackFreqSeconds,
  DODownloadProperty_NoProgressTimeoutSeconds,
  DODownloadProperty_ForegroundPriority,
  DODownloadProperty_BlockingMode,
  DODownloadProperty_CallbackInterface,
  DODownloadProperty_StreamInterface,
  DODownloadProperty_SecurityContext,
  DODownloadProperty_NetworkToken
  DODownloadProperty_CorrelationVector,
  DODownloadProperty_DecryptionInfo,
  DODownloadProperty_IntegrityCheckInfo,
  DODownloadProperty_IntegrityCheckMandatory,
  DODownloadProperty_TotalSizeBytes
} DODownloadProperty;
```

## <a name="constants"></a>Constantes

| Requisito | Valor |
|-|-|
| DODownloadProperty_Id | Somente leitura. Use essa propriedade para obter a ID que identifica exclusivamente o download. O tipo VARIANT é VT_BSTR. |
| DODownloadProperty_Uri | Use essa propriedade para definir ou obter o caminho de URI remoto do recurso a ser baixado. Essa propriedade será necessária somente *se DODownloadProperty_ContentId* não for fornecido. O tipo VARIANT é VT_BSTR. |
| DODownloadProperty_ContentId | Use essa propriedade para definir ou obter a ID de conteúdo exclusivo do download. Essa propriedade será necessária somente *se DODownloadProperty_Uri* não for fornecido. O tipo VARIANT é VT_BSTR. |
| DODownloadProperty_DisplayName | Opcional. Use essa propriedade para definir ou obter o nome de exibição do download. O tipo VARIANT é VT_BSTR. |
| DODownloadProperty_LocalPath | Use essa propriedade para definir ou obter o nome do caminho local para salvar o arquivo de download. Se o caminho não existir, o DO tentará criar sob os privilégios do chamador. Essa propriedade só será necessária *se DODownloadProperty_StreamInterface* não tiver sido fornecida. O tipo VARIANT é VT_BSTR. |
| DODownloadProperty_HttpCustomHeaders | Opcional. Use essa propriedade para definir ou obter cabeçalhos de solicitação HTTP personalizados. O DO incluirá esses cabeçalhos durante operações de solicitação de arquivo HTTP. Os cabeçalhos já devem ser formatados como cabeçalhos HTTP padrão. O tipo VARIANT é VT_BSTR. |
| DODownloadProperty_CostPolicy | Opcional. Use essa propriedade para definir ou obter um dos valores de enumeração **DODownloadCostPolicy.** O tipo VARIANT é VT_UI4. |
| DODownloadProperty_SecurityFlags | Somente gravação opcional. Use essa propriedade para definir ou obter os sinalizadores de segurança WinHTTP padrão (**WINHTTP_OPTION_SECURITY_FLAGS**). O tipo VARIANT é VT_UI4.</br></br>Há suporte para os seguintes sinalizadores:</br>SECURITY_FLAG_IGNORE_CERT_CN_INVALID. Permite um nome comum inválido em um certificado.</br>SECURITY_FLAG_IGNORE_CERT_DATE_INVALID. Permite uma data de certificado inválida.</br>SECURITY_FLAG_IGNORE_UNKNOWN_CA. Permite uma autoridade de certificação inválida.</br>SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE. Permite que a identidade de um servidor seja estabelecida com um certificado não servidor.</br>WINHTTP_ENABLE_SSL_REVOCATION. Permite a revogação de SSL. Se esse sinalizador for definido, os sinalizadores acima serão ignorados. |
| DODownloadProperty_CallbackFreqPercent | Opcional. Use essa propriedade para definir ou obter a frequência de retorno de chamada com base no percentual de download. O tipo VARIANT é VT_UI4. |
| DODownloadProperty_CallbackFreqSeconds | Opcional. Use essa propriedade para definir ou obter a frequência de retorno de chamada com base no tempo de download. O padrão é a cada um segundo. O tipo VARIANT é VT_UI4. |
| DODownloadProperty_NoProgressTimeoutSeconds | Opcional. Use essa propriedade para definir ou obter o comprimento do tempo-tempo de download sem progresso. O valor mínimo aceito é 60 segundos sem atividade de download. O tipo VARIANT é VT_UI4. |
| DODownloadProperty_ForegroundPriority | Opcional. Use essa propriedade para definir ou obter a prioridade de download atual. VARIANT_TRUE valor colocará o download em primeiro plano com prioridade mais alta. O padrão é a prioridade em segundo plano. O tipo VARIANT é VT_BOOL. |
| DODownloadProperty_BlockingMode | Opcional. Use essa propriedade para definir ou obter o modo de bloqueio de download atual. VARIANT_TRUE valor fará com que **IDODownload::Start bloqueie** até que o download seja concluído ou o erro tenha ocorrido. O padrão é o modo de não desbloqueio. O tipo VARIANT é VT_BOOL. |
| DODownloadProperty_CallbackInterface | Opcional. Use essa propriedade para definir ou obter o ponteiro para a interface **IDODownloadStatusCallback** usada para baixar retornos de chamada. O tipo VARIANT é VT_UNKNOWN. |
| DODownloadProperty_StreamInterface | Opcional. Use essa propriedade para definir ou obter o ponteiro para a interface IStream usada para o tipo de download de fluxo. O tipo VARIANT é VT_UNKNOWN. |
| DODownloadProperty_SecurityContext | Somente gravação opcional. Use essa propriedade para definir o contexto do certificado a ser usado durante operações de solicitação HTTP. O valor deve consistir em bytes serializados de CERT_CONTEXT. O tipo VARIANT é (VT_ARRAY \| VT_UI1). |
| DODownloadProperty_NetworkToken | Somente gravação opcional. Use essa propriedade para definir o token de rede a ser usado durante operações HTTP. VARIANT_TRUE valor fará com que o DO capture o token de identidade do chamador e VARIANT_FALSE limpará o token existente. O padrão é o token do usuário conectado. O tipo VARIANT é VT_BOOL. |
| DODownloadProperty_CorrelationVector | Opcional. Define um vetor de correlação específico para fins de telemetria. O tipo VARIANT é VT_BSTR. |
| DODownloadProperty_DecryptionInfo | Somente gravação opcional. Define informações de descriptografia na forma de uma cadeia de caracteres JSON. O tipo VARIANT é VT_BSTR. |
| DODownloadProperty_IntegrityCheckInfo | Somente gravação opcional. Define o local do PHF (arquivo hash de peça), que é usado pelo DO para executar verificações de integridade de runtime no conteúdo baixado. O tipo VARIANT é VT_BSTR. |
| DODownloadProperty_IntegrityCheckMandatory | Opcional. Define um sinalizador booliana que indica se o uso do PHF (arquivo de hash de peça) é obrigatório. Se VARIANT_TRUE, o download será anulado se a verificação de integridade falhar. O tipo VARIANT é VT_BOOL. |
| DODownloadProperty_TotalSizeBytes | Opcional. Especifica o tamanho total do download em bytes. O tipo VARIANT é VT_UI8. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | \[Windows 10, versão 1809 Somente aplicativos Win32\] |
| **Servidor mínimo com suporte** | Windows Servidor, versão 1809 \[ Somente aplicativos Win32\] |
| **Cabeçalho** | DeliveryOptimizationDownloadTypes.h |
