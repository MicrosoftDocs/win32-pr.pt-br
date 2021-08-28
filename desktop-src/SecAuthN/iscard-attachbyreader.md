---
description: O método AttachByReader abre o cartão inteligente no leitor nomeado.
ms.assetid: a92f3281-5018-4e90-bfa0-f03eb9373bb1
title: Método ISCard::AttachByReader (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.AttachByReader
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b1227c94edbf5816a8f1e867436462a743e6961e3ca70bb7b8a521c289312f18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015676"
---
# <a name="iscardattachbyreader-method"></a>Método ISCard::AttachByReader

\[O **método AttachByReader** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O **método AttachByReader** abre o [*cartão inteligente*](../secgloss/s-gly.md) no leitor [*nomeado.*](../secgloss/r-gly.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AttachByReader(
  [in] BSTR              bstrReaderName,
  [in] SCARD_SHARE_MODES ShareMode,
  [in] SCARD_PROTOCOLS   PrefProtocol
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrReaderName* \[ Em\]
</dt> <dd>

Um **BSTR** que contém o nome do leitor de cartão inteligente.

</dd> <dt>

*ShareMode* \[ Em\]
</dt> <dd>

Modo no qual solicitar acesso ao cartão inteligente.



| Valor                                                                                                                                            | Significado                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <dt>**Exclusivo**</dt> </dl> | Ninguém mais usa essa conexão com o cartão inteligente.<br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <dt>**Compartilhado**</dt> </dl>          | Outros aplicativos podem usar essa conexão.<br/>        |



 

</dd> <dt>

*PrefProtocol* \[ Em\]
</dt> <dd>

Valor de protocolo preferencial.

<dl><span id="T0"></span><span id="t0"></span><dt>

**T0**
</dt><span id="T1"></span><span id="t1"></span><dt>

**T1**
</dt><span id="RAW"></span><span id="raw"></span><dt>

**RAW**
</dt><span id="T0_T1"></span><span id="t0_t1"></span><dt>

**T0 \| T1**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                  | Descrição                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Abrir no cartão inteligente no leitor nomeado foi concluído com êxito.<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Há algo errado com um ou mais dos parâmetros passados para a função.<br/> |



 

## <a name="remarks"></a>Comentários

Além dos códigos de erro COM listados acima, essa interface poderá retornar um código de erro de cartão inteligente se uma função de cartão inteligente tiver sido chamada para concluir [*a*](../secgloss/s-gly.md) solicitação. Para obter mais informações, consulte [Valores de retorno de cartão inteligente](authentication-return-values.md).

Quando terminar de usar o leitor, libere o anexo chamando o [**método ISCard::D etach.**](iscard-detach.md)

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra a anexação a um cartão inteligente em um leitor de cartão inteligente especificado.


```C++
#include <windows.h>
#include <stdio.h>
#include <Scardmgr.h>

// The reader name is vendor specific; change as needed.
#define READER_NAME L"Vendor Reader 0"

void main()
{
    BSTR     bstrReader = NULL;
    HRESULT  hr;

    bstrReader = SysAllocString(READER_NAME);
    if (NULL == bstrReader)
    {
        // Error encountered.
        exit(1);
    }

    // Connect to the reader.
    hr = pISCard->AttachByReader(bstrReader, SHARED, T0);
    if (FAILED(hr))
    {
        printf("Failed AttachByReader\n");
        // Take other error handling action.
        // ...
    }

    // Detach reader by calling ISCard::Detach (not shown).
    // ...

    // When done, free BSTR.
    if (NULL != bstrReader)
        SysFreeString(bstrReader);
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCard é definido como \_ 1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**AttachByHandle**](iscard-attachbyhandle.md)
</dt> <dt>

[**Detach**](iscard-detach.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> <dt>

[**Reanexar**](iscard-reattach.md)
</dt> </dl>

 

 
