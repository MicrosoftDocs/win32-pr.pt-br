---
description: A função PdhVbCreateCounterPathList exibe a caixa de diálogo de navegação do contador de desempenho, que permite ao usuário selecionar vários contadores de desempenho. Cada caminho de contador selecionado deve ser lido usando a função PdhVbGetCounterPathFromList.
ms.assetid: 8dda528f-2e06-4726-89a0-095781a2f80d
title: Função PdhVbCreateCounterPathList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbCreateCounterPathList
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: bef484846507bf68d8ccfc0ad3ea10a250b83133
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828388"
---
# <a name="pdhvbcreatecounterpathlist-function"></a>Função PdhVbCreateCounterPathList

A função **PdhVbCreateCounterPathList** exibe a caixa de diálogo de navegação do contador de desempenho, que permite ao usuário selecionar vários contadores de desempenho. Cada caminho de contador selecionado deve ser lido usando a função [**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md) .

> [!IMPORTANT]
> A função que este tópico descreve pode ser alterada ou indisponível no futuro. Em vez disso, a Microsoft recomenda que você use as funções descritas em [funções de contadores de desempenho](performance-counters-functions.md).

Função PdhVbCreateCounterPathList ( \_ ByVal DetailLevel as Long, \_ ByVal Legendastring as String \_ ) como Long

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DetailLevel* 
</dt> <dd>

Tipos de contadores a serem exibidos na caixa de diálogo. Use um dos valores a seguir.



| Valor                                                                                                                                                                               | Significado                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PERF_DETAIL_ADVANCED"></span><span id="perf_detail_advanced"></span><dl> <dt>**detalhes do desempenho \_ \_ avançado**</dt> </dl> | Os contadores que o usuário avançado provavelmente entenderá, além dos contadores de usuário iniciantes.<br/>                                            |
| <span id="PERF_DETAIL_EXPERT"></span><span id="perf_detail_expert"></span><dl> <dt>**\_especialista em detalhes de desempenho \_**</dt> </dl>       | Os contadores que o usuário experiente e o desenvolvedor de software provavelmente compreenderão, além dos contadores para os usuários iniciantes e avançados.<br/> |
| <span id="PERF_DETAIL_NOVICE"></span><span id="perf_detail_novice"></span><dl> <dt>**reiniciante de detalhes de desempenho \_ \_**</dt> </dl>       | Somente os contadores que o usuário iniciante provavelmente entenderá.<br/>                                                                                  |
| <span id="PERF_DETAIL_WIZARD"></span><span id="perf_detail_wizard"></span><dl> <dt>**\_Assistente de detalhes de desempenho \_**</dt> </dl>       | Todos os contadores no sistema.<br/>                                                                                                                  |



 

</dd> <dt>

*Legendastring* 
</dt> <dd>

Variável de cadeia de caracteres que contém o texto que será exibido na barra de legenda da caixa de diálogo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna o número de caminhos do contador que o usuário selecionou.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
</dt> <dt>

[**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




