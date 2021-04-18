---
description: A implementação dessa interface é fornecida como um código de exemplo com o SDK do DirectShow.
ms.assetid: a18fc6b6-f37e-4c87-9150-0504333d33c2
title: Interface IMpeg2PsiParser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser
api_type:
- COM
api_location: ''
ms.openlocfilehash: 51f0f3373c67da75c50ecc2f6bc234e0351f5dc3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105754760"
---
# <a name="impeg2psiparser-interface"></a>Interface IMpeg2PsiParser

A implementação dessa interface é fornecida como um código de exemplo com o SDK do DirectShow. Não é uma API do DirectShow com suporte.

A `IMpeg2PsiParser` interface recupera informações específicas do programa (psi) do filtro do analisador psi, que é fornecido no SDK do DirectShow como um filtro de exemplo. Um aplicativo pode usar esse filtro para mapear IDs de programa (PIDs) no filtro de demultiplexador MPEG-2.

## <a name="members"></a>Membros

A interface **IMpeg2PsiParser** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IMpeg2PsiParser** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IMpeg2PsiParser** tem esses métodos.



| Método                                                                             | Descrição                                                                               |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**FindRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd407137(v=vs.85))         | Localiza o PID da tabela de mapa do programa (PGTO) para um programa, dado o número do programa.<br/> |
| [**GetCountOfElementaryStreams**](impeg2psiparser-getcountofelementarystreams.md) | Recupera o número de fluxos elementares em um programa especificado.<br/>             |
| [**GetCountOfPrograms**](impeg2psiparser-getcountofprograms.md)                   | Recupera o número de programas no fluxo de transporte.<br/>                      |
| [**GetPatVersionNumber**](impeg2psiparser-getpatversionnumber.md)                 | Recupera o \_ campo de número de versão da Pat (tabela de associação de programa).<br/>  |
| [**GetPmtVersionNumber**](impeg2psiparser-getpmtversionnumber.md)                 | Recupera o \_ campo de número de versão de um PGTO especificado.<br/>                      |
| [**GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85))           | Recupera a atribuição de PID para um fluxo elementar especificado em um programa.<br/>   |
| [**GetRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd376624(v=vs.85))           | Recupera a atribuição de PID para um PGTO especificado.<br/>                              |
| [**GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md)           | Recupera o número do programa de um programa especificado.<br/>                          |
| [**GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85))                 | Recupera o tipo de fluxo para um fluxo elementar especificado em um programa.<br/>      |
| [**GetTransportStreamId**](impeg2psiparser-gettransportstreamid.md)               | Recupera o \_ \_ campo ID do fluxo de transporte do Pat.<br/>                        |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Exemplo de filtro do analisador PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 
