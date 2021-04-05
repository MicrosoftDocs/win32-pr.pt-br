---
title: Enumeração dobaixeproperty
description: Especifica a ID das propriedades para a operação de download.
keywords:
- Enumeração dobaixeproperty, dobaixeproperty
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
ms.openlocfilehash: bb8ec6ad8cc55239522f953c6a81a8bf7b2b62ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086107"
---
# <a name="dodownloadproperty-enumeration"></a>Enumeração dobaixeproperty

A enumeração **Dodownloadsproperty** especifica a ID das propriedades para a operação de download. Essa enumeração é usada pela interface **IDODownload** e executada por um valor Variant, onde o tipo de valor está contido.

## <a name="syntax"></a>Syntax

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
| DODownloadProperty_Id | Somente leitura. Use essa propriedade para obter a ID que identifica exclusivamente o download. O tipo de variante é VT_BSTR. |
| DODownloadProperty_Uri | Use essa propriedade para definir ou obter o caminho do URI remoto do recurso a ser baixado. Essa propriedade será necessária somente se *DODownloadProperty_ContentId* não for fornecida. O tipo de variante é VT_BSTR. |
| DODownloadProperty_ContentId | Use essa propriedade para definir ou obter a ID de conteúdo exclusiva de download. Essa propriedade será necessária somente se *DODownloadProperty_Uri* não for fornecida. O tipo de variante é VT_BSTR. |
| DODownloadProperty_DisplayName | Opcional. Use essa propriedade para definir ou obter o nome de exibição de download. O tipo de variante é VT_BSTR. |
| DODownloadProperty_LocalPath | Use essa propriedade para definir ou obter o nome do caminho local para salvar o arquivo de download. Se o caminho não existir, o tentará criá-lo sob os privilégios do chamador. Essa propriedade será necessária somente se *DODownloadProperty_StreamInterface* não tiver sido fornecida. O tipo de variante é VT_BSTR. |
| DODownloadProperty_HttpCustomHeaders | Opcional. Use essa propriedade para definir ou obter cabeçalhos de solicitação HTTP personalizados. Incluirá esses cabeçalhos durante as operações de solicitação de arquivo HTTP. Os cabeçalhos já devem estar formatados como cabeçalhos HTTP padrão. O tipo de variante é VT_BSTR. |
| DODownloadProperty_CostPolicy | Opcional. Use essa propriedade para definir ou obter um dos valores de enumeração **DODownloadCostPolicy** . O tipo de variante é VT_UI4. |
| DODownloadProperty_SecurityFlags | Opcional somente gravação. Use essa propriedade para definir ou obter os sinalizadores de segurança padrão do WinHTTP (**WINHTTP_OPTION_SECURITY_FLAGS**). O tipo de variante é VT_UI4.</br></br>Há suporte para os seguintes sinalizadores:</br>SECURITY_FLAG_IGNORE_CERT_CN_INVALID. Permite um nome comum inválido em um certificado.</br>SECURITY_FLAG_IGNORE_CERT_DATE_INVALID. Permite uma data de certificado inválida.</br>SECURITY_FLAG_IGNORE_UNKNOWN_CA. Permite uma autoridade de certificação inválida.</br>SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE. Permite que a identidade de um servidor seja estabelecida com um certificado que não seja do servidor.</br>WINHTTP_ENABLE_SSL_REVOCATION. Permite a revogação de SSL. Se esse sinalizador for definido, os sinalizadores acima serão ignorados. |
| DODownloadProperty_CallbackFreqPercent | Opcional. Use essa propriedade para definir ou obter a frequência de retorno de chamada com base no percentual de download. O tipo de variante é VT_UI4. |
| DODownloadProperty_CallbackFreqSeconds | Opcional. Use essa propriedade para definir ou obter a frequência de retorno de chamada com base no tempo de download. O padrão é a cada um segundo. O tipo de variante é VT_UI4. |
| DODownloadProperty_NoProgressTimeoutSeconds | Opcional. Use essa propriedade para definir ou obter o comprimento do tempo limite de download para nenhum progresso. O valor mínimo aceito é de 60 segundos de nenhuma atividade de download. O tipo de variante é VT_UI4. |
| DODownloadProperty_ForegroundPriority | Opcional. Use essa propriedade para definir ou obter a prioridade de download atual. VARIANT_TRUE valor levará o download para o primeiro plano com prioridade mais alta. O padrão é a prioridade do plano de fundo. O tipo de variante é VT_BOOL. |
| DODownloadProperty_BlockingMode | Opcional. Use essa propriedade para definir ou obter o modo de bloqueio de download atual. VARIANT_TRUE valor causará **IDODownload:: Start** to Block até que o download seja concluído ou o erro tenha ocorrido. O padrão é o modo de não bloqueio. O tipo de variante é VT_BOOL. |
| DODownloadProperty_CallbackInterface | Opcional. Use essa propriedade para definir ou obter o ponteiro para a interface **IDODownloadStatusCallback** usada para baixar retornos de chamada. O tipo de variante é VT_UNKNOWN. |
| DODownloadProperty_StreamInterface | Opcional. Use essa propriedade para definir ou obter o ponteiro para a interface IStream usada para o tipo de download de fluxo. O tipo de variante é VT_UNKNOWN. |
| DODownloadProperty_SecurityContext | Opcional somente gravação. Use essa propriedade para definir o contexto de certificado a ser usado durante as operações de solicitação HTTP. O valor deve consistir em bytes serializados de CERT_CONTEXT. O tipo de variante é (VT_ARRAY \| VT_UI1). |
| DODownloadProperty_NetworkToken | Opcional somente gravação. Use essa propriedade para definir o token de rede a ser usado durante as operações HTTP. VARIANT_TRUE valor causará a captura do token de identidade do chamador e VARIANT_FALSE limpará o token existente. O padrão é o token do usuário conectado. O tipo de variante é VT_BOOL. |
| DODownloadProperty_CorrelationVector | Opcional. Define um vetor de correlação específico para fins de telemetria. O tipo de variante é VT_BSTR. |
| DODownloadProperty_DecryptionInfo | Opcional somente gravação. Define informações de descriptografia na forma de uma cadeia de caracteres JSON. O tipo de variante é VT_BSTR. |
| DODownloadProperty_IntegrityCheckInfo | Opcional somente gravação. Define o local do arquivo de hash da parte (PHF), que é usado pelo para executar verificações de integridade de tempo de execução no conteúdo baixado. O tipo de variante é VT_BSTR. |
| DODownloadProperty_IntegrityCheckMandatory | Opcional. Define um sinalizador booliano que indica se o uso do arquivo de hash da parte (PHF) é obrigatório. Se VARIANT_TRUE, o download será anulado se a verificação de integridade falhar. O tipo de variante é VT_BOOL. |
| DODownloadProperty_TotalSizeBytes | Opcional. Especifica o tamanho total do download em bytes. O tipo de variante é VT_UI8. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | Somente aplicativos do Windows 10, versão 1809 \[ Win32\] |
| **Servidor mínimo com suporte** | Somente aplicativos do Windows Server, versão 1809 \[ Win32\] |
| **Cabeçalho** | DeliveryOptimizationDownloadTypes. h |
