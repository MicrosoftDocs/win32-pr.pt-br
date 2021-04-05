---
title: Compartimentos predefinidos (Ctffunc. h)
description: Os valores a seguir identificam compartimentos implementados pela estrutura de serviços de texto.
ms.assetid: 65177979-ff91-4f62-8ba5-3c426b221b6c
keywords:
- Estrutura de serviços de texto de compartimentos predefinidos
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
ms.openlocfilehash: 9fcc684c4aee55c3c2e1807458ee261ad55156e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086126"
---
# <a name="predefined-compartments"></a>Compartimentos predefinidos

Os valores a seguir identificam compartimentos implementados pela estrutura de serviços de texto.

Os seguintes identificadores de compartimento são definidos em Ctffunc. idl e Ctffunc. h.



| Sinalizador                                     | Valor  | Descrição                                                                                                                                                                                                                                                                               |
|------------------------------------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ áudio SAPI do compartimento de GUID \_           | \_I4 VT | Um **DWORD** que será zero se o áudio de Speech API (SAPI) estiver desativado ou diferente de zero se o áudio SAPI estiver ativado. Esse compartimento é específico para um objeto do Gerenciador de threads.                                                                                                                               |
| \_CFGMENU de \_ fala do compartimento de GUID \_       | \_I4 VT | Um **DWORD** que será zero se o menu de configuração de fala não estiver disponível ou for diferente de zero se o menu de configuração de fala estiver disponível. Esse compartimento é específico para um objeto do Gerenciador de threads.                                                                                               |
| \_DICTATIONSTAT de \_ fala do compartimento de GUID \_ | \_I4 VT | Um valor **DWORD** que contém zero ou uma combinação de um ou mais do [**\_ ditado TF \_ habilitado**](speech-recognition-constants.md), **\_ comando TF \_ habilitado**, **TF \_ ditado \_** ou **TF \_ comando \_ em** valores. Esse compartimento é específico para um objeto do Gerenciador de threads. |
| \_ \_ \_ status da interface do usuário de fala do compartimento GUID \_    | \_I4 VT | Um valor **DWORD** que contém zero ou uma combinação de um ou mais dos valores de balão [**TF \_ show \_ Balloon**](speech-recognition-constants.md) ou **TF \_ Disable \_** . Esse é um compartimento global.                                                                                   |



 

Os seguintes identificadores de compartimento são definidos em MSCTF. IDL e MSCTF. H.



| Sinalizador                                                    | Valor  | Descrição                                                                                                                                                                                                                                                   |
|---------------------------------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| compartimento de GUID \_ \_ EMPTYCONTEXT                         | \_I4 VT | Um **DWORD** que é diferente de zero se o contexto estiver vazio ou nenhum outro. Esse compartimento é específico para um objeto de contexto.                                                                                                                                      |
| \_OPENCLOSE de \_ manuscrito do compartimento de GUID \_               | \_I4 VT | Um **DWORD** que é diferente de zero se o reconhecimento de manuscrito for aberto ou zero se o reconhecimento de manuscrito for fechado. Esse compartimento é específico para um objeto do Gerenciador de threads.                                                                                 |
| teclado de compartimento de GUID \_ \_ \_ desabilitado                   | \_I4 VT | Um **DWORD** que é diferente de zero se o teclado estiver desabilitado ou nenhum outro. Esse compartimento é específico para um objeto de contexto.                                                                                                                                  |
| conversão de teclado do compartimento de GUID de \_ \_ \_ entrada \_      | \_I4 VT | Um valor **DWORD** da combinação correta de [**TF \_ conversõesmode \_**](flags-for-conversion-mode.md) . Esse compartimento é específico para um objeto do Gerenciador de threads.                                                                                      |
| sentença do teclado do compartimento de GUID de \_ \_ \_ entrada \_        | \_I4 VT | Um valor **DWORD** de [**TF \_ frasemode \_**](flags-for-conversion-mode.md). Esse compartimento é específico para um objeto do Gerenciador de threads.                                                                                                                        |
| \_OPENCLOSE de \_ teclado do compartimento de GUID \_                  | \_I4 VT | Um **DWORD** que é diferente de zero se o teclado estiver aberto ou zero se o teclado estiver fechado. Esse compartimento é específico para um objeto do Gerenciador de threads.                                                                                                               |
| compartimento de GUID \_ \_ PERSISTMENUENABLED                   | \_I4 VT | Um **DWORD** que é diferente de zero para fazer com que o serviço de texto de fala habilite o item de menu **salvar dados de fala** ou zero para desabilitá-lo. Esse compartimento é específico para um objeto do Gerenciador de documentos.                                                                   |
| Fala do compartimento de GUID \_ \_ \_ desabilitada                     | \_I4 VT | Um **DWORD** que contém zero ou uma combinação de uma ou mais das [**TF \_ desabilitar \_ fala**](speech-recognition-constants.md), **TF \_ desabilitar \_ ditado** ou **TF \_ desabilitar \_** valores de comando. Esse compartimento é específico para um objeto do Gerenciador de threads. |
| \_OPENCLOSE de \_ fala do compartimento de GUID \_                    | \_I4 VT | Um **DWORD** que seja diferente de zero se a entrada de fala estiver ativa ou zero se a entrada de fala estiver inativa. Esse é um compartimento global.                                                                                                                                      |
| compartimento de GUID \_ \_ TIPUISTATUS                          | \_I4 VT | Não usado no momento.                                                                                                                                                                                                                                           |
| compartimento de GUID \_ \_ TRANSITORYEXTENSION                  | \_I4 VT | Um valor **DWORD** de [**TF \_ TRANSITORYEXTENSION \_ None**](values-for-guid-compartment-transitoryextension.md), **TF \_ TRANSITORYEXTENSION \_ flutuante** ou **TF \_ TRANSITORYEXTENSION \_ ATSELECTION**. Esse compartimento é específico para um objeto do Gerenciador de documentos.  |
| compartimento de GUID \_ \_ TRANSITORYEXTENSION \_ DocumentManager | \_I4 VT | Um valor IUnknown para a interface [**ITfDocumentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) que faz referência ao documento transitório deste Gerenciador de documentos. Esse compartimento é específico para um objeto do Gerenciador de documentos.                                                         |
| compartimento de GUID \_ \_ TRANSITORYEXTENSION \_ pai          | \_I4 VT | Um valor IUnknown para a interface [**ITfDocumentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) que se refere ao Gerenciador de documentos pai deste documento transitório. Esse compartimento é específico para um objeto do Gerenciador de documentos.                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                                                                                          |
| parâmetro<br/>                   | <dl> <dt>Ctffunc. h; </dt> <dt>Mstctf. h</dt> </dl>     |
| INSERI<br/>                      | <dl> <dt>Ctffunc. idl; </dt> <dt>Mstctf. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Constantes de reconhecimento de fala**](speech-recognition-constants.md)
</dt> </dl>

 

 





