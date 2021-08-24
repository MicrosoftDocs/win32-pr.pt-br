---
title: Método IDeliveryOptimizationJob AddFileWithRanges (Deliveryoptimization.h)
description: Adiciona um arquivo a um trabalho de download e especifica os intervalos do arquivo que você deseja baixar.
ms.assetid: 23F0A39F-670F-4030-A3B3-4F9277FFA8AB
keywords:
- Método AddFileWithRanges
- Método AddFileWithRanges, interface IDeliveryOptimizationJob
- Interface IDeliveryOptimizationJob, método AddFileWithRanges
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob.AddFileWithRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 197aa7443123c81d1a675d321b91573823a84f15
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476122"
---
# <a name="ideliveryoptimizationjobaddfilewithranges-method"></a>Método IDeliveryOptimizationJob::AddFileWithRanges

Adiciona um arquivo a um trabalho de download e especifica os intervalos do arquivo que você deseja baixar.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddFileWithRanges(
  [in]           LPCWSTR       fileId,
  [in]           LPCWSTR       remoteUrl,
  [in]           LPCWSTR       localName,
  [in, optional] DWORD         rangeCount,
  [in, optional] BG_FILE_RANGE ranges[],
  [in, optional] ULONG64       fileSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fileId* \[ Em\]
</dt> <dd>

Cadeia de caracteres terminada em nulo que é um identificador exclusivo do conteúdo publicado. Para conteúdo não publicado, pode ser qualquer cadeia de caracteres exclusiva que o chamador possa usar para identificar arquivos em um trabalho.

</dd> <dt>

*remoteUrl* \[ Em\]
</dt> <dd>

Cadeia de caracteres terminada em nulo que contém o nome do arquivo no servidor.

</dd> <dt>

*localName* \[ Em\]
</dt> <dd>

Cadeia de caracteres terminada em nulo que contém o nome do arquivo no cliente.

</dd> <dt>

*rangeCount* \[ in, opcional\]
</dt> <dd>

Número de elementos em *Intervalos*.

</dd> <dt>

*intervalos* \[ in, opcional\]
</dt> <dd>

Matriz de uma ou mais [**BG_FILE_RANGE**](/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range) estruturas que especificam os intervalos a baixar. Não especifique intervalos duplicados ou sobrepostos.

</dd> <dt>

*fileSize* \[ in, opcional\]
</dt> <dd>

Tamanho do arquivo em bytes. Passe o **DO_UNKNOWN_FILE_SIZE** se o tamanho não for conhecido para o aplicativo chamador.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna os seguintes valores de retorno, bem como outros.




| Código de retorno | Descrição | 
|-------------|-------------|
| <dl><dt><strong><strong>S_OK</strong></strong></dt></dl> | Êxito.<br /> | 
| <dl><dt><strong>E_INVALIDARG</strong></dt></dl> | O nome do arquivo local é NULL ou cadeia de caracteres vazia. <br /> | 
| <dl><dt><strong>E_ACCESSDENIED</strong></dt></dl> | O usuário não tem permissão para gravar no diretório especificado no cliente.<br /> | 
| <dl><dt><strong>DO_E_INVALID_RANGE</strong></dt></dl> | Um dos intervalos é inválido. Por exemplo, InitialOffset é definido como <strong>BG_LENGTH_TO_EOF</strong>.<br /> | 
| <dl><dt><strong>DO_E_OVERLAPPING_RANGES</strong></dt></dl> | Não é possível especificar intervalos duplicados ou sobrepostos. <br /><blockquote>[!Note]<br />Os intervalos são classificação pelo deslocamento do valor, não pelo comprimento. Se os intervalos são inseridos que têm o mesmo deslocamento, mas estão na ordem inversa, esse erro será retornado. Por exemplo, se 100.5 e 100.0 são inseridos nessa ordem, você não poderá adicionar o arquivo ao trabalho.</blockquote><br /> | 
| <dl><dt><strong>DO_E_INVALID_STATE</strong></dt></dl> | O estado do trabalho não pode ser <strong>BG_JOB_STATE_CANCELLED</strong> ou <strong>BG_JOB_STATE_ACKNOWLEDGED</strong>.<br /> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, somente aplicativos da área de trabalho versão 1709 \[\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 somente \[ aplicativos da área de trabalho\]<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationJob é definido como EE2584CF-A69C-4848-B633-2649962B3EF7<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDeliveryOptimizationJob**](ideliveryoptimizationjob.md)
</dt> </dl>

 

