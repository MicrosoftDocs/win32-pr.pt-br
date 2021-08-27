---
title: Compartimentos predefinidos (Ctffunc.h)
description: Os valores a seguir identificam compartimentos implementados por Estrutura de Serviços de Texto.
ms.assetid: 65177979-ff91-4f62-8ba5-3c426b221b6c
keywords:
- Compartimentos predefinidos Estrutura de Serviços de Texto
topic_type:
- apiref
api_name:
- Predefined Compartments
api_location:
- Ctffunc.h
- Mstctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c7c59312f7511c093f0d4c51bbdb9491f44b17cd16475e2b4261eaa676836e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118876178"
---
# <a name="predefined-compartments"></a>Compartimentos predefinidos

Os valores a seguir identificam compartimentos implementados por Estrutura de Serviços de Texto.

Os seguintes identificadores de compartimento são definidos em Ctffunc.idl e Ctffunc.h.



| Sinalizador                                     | Valor  | Descrição                                                                                                                                                                                                                                                                               |
|------------------------------------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID \_ COMPARTMENT \_ SAPI \_ AUDIO           | VT \_ I4 | Um **DWORD** que será zero se o Speech API sapi (SAPI) estiver desligado ou não for zero se o áudio SAPI estiver. Esse compartimento é específico para um objeto do gerenciador de threads.                                                                                                                               |
| \_ \_ CFGMENU DE \_ FALA DO COMPARTIMENTO GUID       | VT \_ I4 | Um **DWORD** que será zero se o menu de configuração de fala não estiver disponível ou diferente de zero se o menu de configuração de fala estiver disponível. Esse compartimento é específico para um objeto do gerenciador de threads.                                                                                               |
| GUID \_ COMPARTMENT \_ SPEECH \_ DICTATIONSTAT | VT \_ I4 | Um valor **DWORD** que contém zero ou uma combinação de um ou mais dos valores [**TF \_ DICTATION \_ ENABLED**](speech-recognition-constants.md), **TF \_ COMMANDING \_ ENABLED**, **TF \_ DICTATION \_ ON** ou **TF \_ COMMANDING \_ ON.** Esse compartimento é específico para um objeto do gerenciador de threads. |
| STATUS \_ DA INTERFACE DO USUÁRIO DE FALA DO COMPARTIMENTO \_ \_ \_ GUID    | VT \_ I4 | Um **valor DWORD** que contém zero ou uma combinação de um ou mais dos valores [**TF SHOW \_ \_ BALLOON**](speech-recognition-constants.md) ou **TF DISABLE \_ \_ BALLOON.** Esse é um compartimento global.                                                                                   |



 

Os seguintes identificadores de compartimento são definidos em MSCTF. IDL e MSCTF.H.



| Sinalizador                                                    | Valor  | Descrição                                                                                                                                                                                                                                                   |
|---------------------------------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID \_ COMPARTMENT \_ EMPTYCONTEXT                         | VT \_ I4 | Uma **DWORD** diferente de zero se o contexto estiver vazio ou zero, caso contrário. Esse compartimento é específico para um objeto de contexto.                                                                                                                                      |
| GUID \_ COMPARTMENT \_ HANDWRITING \_ OPENCLOSE               | VT \_ I4 | Um **DWORD** que não será zero se o reconhecimento de manuscrito estiver aberto ou zero se o reconhecimento de manuscrito estiver fechado. Esse compartimento é específico para um objeto do gerenciador de threads.                                                                                 |
| TECLADO \_ DO COMPARTIMENTO GUID \_ \_ DESABILITADO                   | VT \_ I4 | Um **DWORD** diferente de zero se o teclado estiver desabilitado ou zero, caso contrário. Esse compartimento é específico para um objeto de contexto.                                                                                                                                  |
| CONVERSÃO \_ DE \_ \_ INPUTMODE DO TECLADO DO COMPARTIMENTO \_ GUID      | VT \_ I4 | Um **valor DWORD** da combinação adequada de sinalizadores [**TF \_ CONVERSIONMODE. \_**](flags-for-conversion-mode.md) Esse compartimento é específico para um objeto do gerenciador de threads.                                                                                      |
| GUID \_ COMPARTMENT \_ KEYBOARD \_ INPUTMODE \_ SENTENCE        | VT \_ I4 | Um **valor DWORD** de [**TF \_ SENTENCEMODE. \_**](flags-for-conversion-mode.md) Esse compartimento é específico para um objeto do gerenciador de threads.                                                                                                                        |
| GUID \_ COMPARTMENT \_ KEYBOARD \_ OPENCLOSE                  | VT \_ I4 | Um **DWORD** que não será zero se o teclado estiver aberto ou zero se o teclado estiver fechado. Esse compartimento é específico para um objeto do gerenciador de threads.                                                                                                               |
| GUID \_ COMPARTMENT \_ PERSISTMENUENABLED                   | VT \_ I4 | Uma **DWORD** que não é zero para fazer com que o serviço de texto de fala habilita o **item** de menu Salvar Dados de Fala ou zero para desabilitá-lo. Esse compartimento é específico para um objeto do gerenciador de documentos.                                                                   |
| GUID \_ COMPARTIMENTO DE FALA \_ \_ DESABILITADO                     | VT \_ I4 | Uma **DWORD que** contém zero ou uma combinação de um ou mais dos valores [**TF DISABLE \_ \_ SPEECH**](speech-recognition-constants.md), **TF DISABLE \_ \_ DICTATION** ou **TF DISABLE \_ \_ COMMANDING.** Esse compartimento é específico para um objeto do gerenciador de threads. |
| GUID \_ COMPARTIMENTO DE FALA \_ \_ OPENCLOSE                    | VT \_ I4 | Uma **DWORD** que não será zero se a entrada de fala estiver ativa ou zero se a entrada de fala estiver inativa. Esse é um compartimento global.                                                                                                                                      |
| GUID \_ COMPARTMENT \_ TIPUISTATUS                          | VT \_ I4 | Não usado no momento.                                                                                                                                                                                                                                           |
| GUID \_ COMPARTMENT \_ TRANSITORYEXTENSION                  | VT \_ I4 | Um **valor DWORD** de [**TF \_ TRANSITORYEXTENSION \_ NONE**](values-for-guid-compartment-transitoryextension.md), **TF \_ TRANSITORYEXTENSION \_ FLOATING** ou **TF \_ TRANSITORYEXTENSION \_ ATSELECTION**. Esse compartimento é específico para um objeto do gerenciador de documentos.  |
| GUID \_ COMPARTMENT \_ TRANSITORYEXTENSION \_ DOCUMENTMANAGER | VT \_ I4 | Um valor IUnknown para a interface [**ITfDocumentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) que se refere ao documento transitório deste gerenciador de documentos. Esse compartimento é específico para um objeto do gerenciador de documentos.                                                         |
| GUID \_ COMPARTMENT \_ TRANSITORYEXTENSION \_ PARENT          | VT \_ I4 | Um valor IUnknown para a interface [**ITfDocumentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) que se refere ao gerenciador de documentos pai deste documento transitório. Esse compartimento é específico para um objeto do gerenciador de documentos.                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Redistribuível<br/>          | TSF 1.0 no Windows 2000 Professional<br/>                                                                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Ctffunc.h; </dt> <dt>Mstctf.h</dt> </dl>     |
| Idl<br/>                      | <dl> <dt>Ctffunc.idl; </dt> <dt>Mstctf.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Constantes de reconhecimento de fala**](speech-recognition-constants.md)
</dt> </dl>

 

 





