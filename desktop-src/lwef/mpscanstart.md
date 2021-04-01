---
title: Função MpScanStart (MpClient. h)
description: Inicia uma operação de verificação.
ms.assetid: 3AF147C8-A41F-4193-AE28-72C1FBD18BA2
keywords:
- Recursos do ambiente Windows herdado da função MpScanStart
topic_type:
- apiref
api_name:
- MpScanStart
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d343787edc85a18dc7471d19165999a7252d18a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918716"
---
# <a name="mpscanstart-function"></a>Função MpScanStart

Inicia uma operação de verificação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI MpScanStart(
  _In_     MPHANDLE          hMpHandle,
  _In_     MPSCAN_TYPE       ScanType,
  _In_     DWORD             dwScanOptions,
  _In_opt_ PMPSCAN_RESOURCES pScanResources,
  _In_opt_ PMPCALLBACK_INFO  pCallbackInfo,
  _Out_    PMPHANDLE         phScanHandle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hMpHandle* \[ no\]
</dt> <dd>

Tipo: **MPHANDLE**

Identificador para a interface do Malware Protection Manager. Esse identificador é retornado pela função [**MpManagerOpen**](mpmanageropen.md) .

</dd> <dt>

*Examinartype* \[ no\]
</dt> <dd>

Tipo: **[ **\_ tipo de MPSCAN**](mpscan-type.md)**

Especifica o tipo de verificação. Esse parâmetro deve ser um dos membros do [**\_ tipo MPSCAN**](mpscan-type.md) enueration.

</dd> <dt>

*dwScanOptions* \[ no\]
</dt> <dd>

Tipo: **DWORD**

Especifica várias opções para a operação de verificação.



| Valor                                                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPSCAN_OPTION_NONE"></span><span id="mpscan_option_none"></span><dl> <dt>**\_opção MPSCAN \_ None**</dt> </dl>                               | Nenhuma opção específica é solicitada.<br/>                                                                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_ASYNC"></span><span id="mpscan_option_async"></span><dl> <dt>**\_opção MPSCAN \_ Async**</dt> </dl>                            | A operação de verificação é assíncrona, em que **MpScanStart** retorna imediatamente após o início bem-sucedido da verificação. (Por padrão, a operação de verificação é síncrona, o que significa que **MpScanStart** retornará somente depois que a verificação for concluída.)<br/>      |
| <span id="MPSCAN_OPTION_PROGRESS"></span><span id="mpscan_option_progress"></span><dl> <dt>**\_progresso da opção MPSCAN \_**</dt> </dl>                   | O chamador está interessado em receber informações de progresso da verificação por meio de um retorno de chamada.<br/>                                                                                                                                                                            |
| <span id="MPSCAN_OPTION_LOWPRIORITY"></span><span id="mpscan_option_lowpriority"></span><dl> <dt>**MPSCAN \_ opção \_ LOWPRIORITY**</dt> </dl>          | Execute a verificação com baixa prioridade. (Por padrão, a operação de verificação é executada com prioridade normal.)<br/>                                                                                                                                                     |
| <span id="MPSCAN_OPTION_PACKEDEXES"></span><span id="mpscan_option_packedexes"></span><dl> <dt>**MPSCAN \_ opção \_ PACKEDEXES**</dt> </dl>             | Examine os executáveis empacotados para possíveis ameaças.<br/>                                                                                                                                                                                                              |
| <span id="MPSCAN_OPTION_ARCHIVES"></span><span id="mpscan_option_archives"></span><dl> <dt>**\_arquivos mortos de opção MPSCAN \_**</dt> </dl>                   | Examinar o conteúdo do arquivo para possíveis ameaças. Arquivos com extensões como. zip,. cab ou. tar.<br/>                                                                                                                                                |
| <span id="MPSCAN_OPTION_HEURISTICS"></span><span id="mpscan_option_heuristics"></span><dl> <dt>**\_heurística da opção MPSCAN \_**</dt> </dl>             | Habilite a verificação baseada em heurística. Isso verificará se há ameaças com o tipo de detecção definido como heurística.<br/>                                                                                                                                                        |
| <span id="MPSCAN_OPTION_REPORTFRIENDLY"></span><span id="mpscan_option_reportfriendly"></span><dl> <dt>**MPSCAN \_ opção \_ REPORTFRIENDLY**</dt> </dl> | Relatar itens amigáveis em uma verificação de recurso. Isso se destina somente ao uso interno.<br/>                                                                                                                                                                          |
| <span id="MPSCAN_OPTION_REPORTUNKNOWN"></span><span id="mpscan_option_reportunknown"></span><dl> <dt>**MPSCAN \_ opção \_ REPORTUNKNOWN**</dt> </dl>    | Relatar itens desconhecidos em uma verificação de recurso. Isso se destina somente ao uso interno.<br/>                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_NOCONSOLIDATE"></span><span id="mpscan_option_noconsolidate"></span><dl> <dt>**\_opção MPSCAN \_ noconsolidate**</dt> </dl>    | Não consolide os resultados da verificação com a exibição de ameaça global. Isso é útil para um cliente (como um cliente de email) que deseja controlar a experiência de limpeza por si só, em vez de permitir a experiência de limpeza Antimalware padrão. Isso se destina somente ao uso interno.<br/> |



 

</dd> <dt>

*pScanResources* \[ em, opcional\]
</dt> <dd>

Tipo: **\_ recursos de PMPSCAN**

Um ponteiro para as informações do recurso de verificação. Esse parâmetro deve ser **nulo** para uma verificação rápida. Esse é um parâmetro opcional para uma verificação completa. Para uma verificação de recurso, esse parâmetro deve ser especificado com pelo menos uma estrutura de informações de recurso. Para verificar recursos específicos, o chamador deve ter a permissão de **\_ leitura genérica** para o recurso. Consulte [**\_ recursos do MPSCAN**](mpscan-resources.md).

</dd> <dt>

*pCallbackInfo* \[ em, opcional\]
</dt> <dd>

Tipo: **\_ informações de PMPCALLBACK**

Um ponteiro para as informações de retorno de chamada usadas para alimentar o cliente com alterações de estado de verificação (como iniciar e concluir) e informações de progresso. Os [**\_ dados de MPCALLBACK**](mpcallback-data.md) passados na função de retorno de chamada relatam o estado de verificação real e as informações relacionadas ao progresso. Veja a seguir uma lista de possíveis retornos de chamada:



| Valor                                                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span><dl> <dt>**\_início da verificação de mpnotify \_**</dt> </dl>                            | Operação de verificação iniciada.<br/>                                                                                                                                                                                                                                                                                       |
| <span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span><dl> <dt>**verificação de MPNOTIFY \_ \_ concluída**</dt> </dl>                   | Operação de verificação concluída. Informações adicionais estão disponíveis por meio da estrutura de [**\_ dados MPSCAN**](mpscan-data.md) .<br/>                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span><dl> <dt>**verificação de MPNOTIFY \_ \_ pausada**</dt> </dl>                         | A operação de verificação está em pausa.<br/>                                                                                                                                                                                                                                                                                     |
| <span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span><dl> <dt>**verificação do MPNOTIFY \_ \_ retomada**</dt> </dl>                      | A operação de verificação foi retomada da pausa.<br/>                                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span><dl> <dt>**MPNOTIFY de \_ verificação \_ cancelada**</dt> </dl>                         | A operação de verificação foi cancelada.<br/>                                                                                                                                                                                                                                                                                 |
| <span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span><dl> <dt>**\_progresso da verificação de mpnotify \_**</dt> </dl>                   | Informações de progresso da verificação. Informações adicionais (como estatísticas de recursos) estão disponíveis por meio da estrutura de [**\_ dados MPSCAN**](mpscan-data.md) .<br/>                                                                                                                                                               |
| <span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span><dl> <dt>**\_erro de verificação de mpnotify \_**</dt> </dl>                            | Verificar informações de erro de um recurso específico. As informações específicas do recurso estão disponíveis por meio da estrutura de [**\_ dados do MPSCAN**](mpscan-data.md) .<br/>                                                                                                                                                             |
| <span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span><dl> <dt>**verificação de MPNOTIFY \_ \_ infectada**</dt> </dl>                   | A verificação encontrou um recurso infectado. Observe que, na maioria dos casos, isso resultará em alguma ameaça relatada no final da verificação. Às vezes, ele não pode materializar como uma ameaça devido a exclusões. Informações adicionais sobre recursos infectados estão disponíveis por meio da estrutura de [**\_ dados do MPSCAN**](mpscan-data.md) .<br/> |
| <span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span><dl> <dt>**MPNOTIFY \_ Scan \_ MEMORYSTART**</dt> </dl>          | A parte de verificação rápida da verificação completa foi iniciada.<br/>                                                                                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span><dl> <dt>**MPNOTIFY \_ Scan \_ MEMORYCOMPLETE**</dt> </dl> | A parte de verificação rápida da verificação completa foi concluída.<br/>                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <dt>**\_falha interna do mpnotify \_**</dt> </dl>          | A operação de verificação encontrou uma falha genérica. O *HRESULT* nos [**\_ dados MPCALLBACK**](mpcallback-data.md) tem o código de erro específico.<br/>                                                                                                                                                                   |



 

</dd> <dt>

*phScanHandle* \[ fora\]
</dt> <dd>

Tipo: **PMPHANDLE**

O identificador de verificação retornado que identifica a verificação iniciada no momento. Esse identificador pode ser usado em chamadas de função subsequentes, como para recuperar um resultado de verificação. O identificador deve ser fechado com a função [**MpHandleClose**](mphandleclose.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se a função for bem sucedido, o valor de retorno será **S \_ OK**.

Se a função falhar, o valor de retorno será um código **HRESULT** com falha. O chamador pode usar a função [**MpErrorMessageFormat**](mperrormessageformat.md) para obter uma descrição genérica da mensagem de erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpHandleClose**](mphandleclose.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**dados do MPCALLBACK \_**](mpcallback-data.md)
</dt> <dt>

[**dados do MPSCAN \_**](mpscan-data.md)
</dt> <dt>

[**recursos do MPSCAN \_**](mpscan-resources.md)
</dt> <dt>

[**tipo de MPSCAN \_**](mpscan-type.md)
</dt> </dl>

 

 





