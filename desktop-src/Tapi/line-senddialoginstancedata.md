---
description: A mensagem de SENDDIALOGINSTANCEDATA da linha TSPI \_ faz com que a TAPI chame a \_ função TUISPI PROVIDERGENERICDIALOGDATA na DLL da interface do usuário associada a htDlgInst, passando a ela o bloco de parâmetro apontado por lpParams, de comprimento dwSize.
ms.assetid: d3c176ba-8b4b-4b7c-a603-130dfa761898
title: Mensagem de LINE_SENDDIALOGINSTANCEDATA (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0af7ae5bfc942d4408ac5ce2438cd9a88c1f1f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792619"
---
# <a name="line_senddialoginstancedata-message"></a>Mensagem de SENDDIALOGINSTANCEDATA de linha \_

A mensagem **de \_ SENDDIALOGINSTANCEDATA da linha** TSPI faz com que a TAPI chame a função [**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) na DLL da interface do usuário associada a *htDlgInst*, passando a ela o bloco de parâmetro apontado por *lpParams*, de comprimento *dwSize*.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*htDlgInst* 
</dt> <dd>

O HTAPIDIALOGINSTANCE que foi retornado ao provedor de serviços quando a instância da caixa de diálogo foi criada usando a [**linha \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md).

</dd> <dt>

*lpParams* 
</dt> <dd>

Ponteiro para um bloco de parâmetro específico de provedor que é transmitido para a função de interface do usuário [**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) , o tamanho especificado por *dwSize*. Se esse parâmetro for definido como **NULL**, essa será uma solicitação para fechar a caixa de diálogo imediatamente e limpar (a DLL da interface do usuário não deve invocar [**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) durante essa limpeza).

</dd> <dt>

*dwSize* 
</dt> <dd>

O tamanho em bytes do bloco de parâmetro a ser transmitido para a DLL da interface do usuário.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
</dt> <dt>

[**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)
</dt> <dt>

[**CREATEDIALOGINSTANCE de linha \_**](line-createdialoginstance.md)
</dt> </dl>

 

