---
title: Método IDeliveryOptimizationJob AddFileWithRanges (Deliveryoptimization. h)
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
ms.openlocfilehash: cc147f5cb3f91a2fe0b8518493dba72798ce8056
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105787637"
---
# <a name="ideliveryoptimizationjobaddfilewithranges-method"></a>Método IDeliveryOptimizationJob:: AddFileWithRanges

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

*FileID* \[ no\]
</dt> <dd>

Cadeia de caracteres terminada em NULL que é um identificador exclusivo do conteúdo publicado. Para conteúdo não publicado, pode ser qualquer cadeia de caracteres exclusiva que o chamador possa usar para identificar arquivos em um trabalho.

</dd> <dt>

*remoteUrl* \[ no\]
</dt> <dd>

Cadeia de caracteres terminada em nulo que contém o nome do arquivo no servidor.

</dd> <dt>

*LocalName* \[ no\]
</dt> <dd>

Cadeia de caracteres terminada em nulo que contém o nome do arquivo no cliente.

</dd> <dt>

*rangeCount* \[ em, opcional\]
</dt> <dd>

Número de elementos em *intervalos*.

</dd> <dt>

*intervalos* \[ de em, opcional\]
</dt> <dd>

Matriz de uma ou mais estruturas de [**BG_FILE_RANGE**](/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range) que especificam os intervalos a serem baixados. Não especifique intervalos duplicados ou sobrepostos.

</dd> <dt>

*tamanho* \[ de um em, opcional\]
</dt> <dd>

Tamanho do arquivo em bytes. Passe **DO_UNKNOWN_FILE_SIZE** se o tamanho não for conhecido pelo aplicativo chamador.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna os seguintes valores de retorno, bem como outros.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Código de retorno</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong><strong>S_OK</strong></strong></dt> </dl></td>
<td>Êxito.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>E_INVALIDARG</strong></dt> </dl></td>
<td>O nome do arquivo local é nulo ou uma cadeia de caracteres vazia. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>E_ACCESSDENIED</strong></dt> </dl></td>
<td>O usuário não tem permissão para gravar no diretório especificado no cliente.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>DO_E_INVALID_RANGE</strong></dt> </dl></td>
<td>Um dos intervalos é inválido. Por exemplo, InitialOffset é definido como <strong>BG_LENGTH_TO_EOF</strong>.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>DO_E_OVERLAPPING_RANGES</strong></dt> </dl></td>
<td>Não é possível especificar intervalos duplicados ou sobrepostos. <br/>
<blockquote>
[!Note]<br />
Os intervalos são classificados pelo deslocamento do valor, não pelo comprimento. Se forem inseridos intervalos com o mesmo deslocamento, mas estiverem na ordem inversa, esse erro será retornado. Por exemplo, se 100,5 e 100,0 forem inseridos nessa ordem, você não poderá adicionar o arquivo ao trabalho.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>DO_E_INVALID_STATE</strong></dt> </dl></td>
<td>O estado do trabalho não pode ser <strong>BG_JOB_STATE_CANCELLED</strong> ou <strong>BG_JOB_STATE_ACKNOWLEDGED</strong>.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationJob é definido como EE2584CF-A69C-4848-B633-2649962B3EF7<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDeliveryOptimizationJob**](ideliveryoptimizationjob.md)
</dt> </dl>

 

