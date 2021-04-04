---
description: Retorna o campo Le da unidade de dados do protocolo de aplicativo (APDU).
ms.assetid: 249e8105-273b-42f0-9427-9b3cda5bf0a1
title: 'Método ISCardCmd:: get_LeField (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_LeField
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bc35f2686a32ce07e1ca630d3ccad3c47b36ca2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663359"
---
# <a name="iscardcmdget_lefield-method"></a>Método ISCardCmd:: get \_ LeField

\[O método **Get \_ LeField** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **Get \_ LeField** retorna o campo Le da APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_LeField(
  [out] LONG *plSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*plSize* \[ fora\]
</dt> <dd>

Ponteiro para o valor do campo Le no retorno.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                  | Descrição                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | A operação foi concluída com êxito.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O parâmetro *plSize* não é válido.<br/>  |



 

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como recuperar o valor do campo Le da APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ). O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .


```C++
LONG     lLe;
HRESULT  hr;

// Retrieve the Le field value.
hr = pISCardCmd->get_LeField(&lLe);
if (FAILED(hr))
{
    printf("Failed get_LeField\n");
    // Take other error handling action.
}
else
    printf("Le field value returned is %d\n", lLe);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Scarddat. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
