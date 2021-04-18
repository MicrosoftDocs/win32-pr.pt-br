---
description: Define o primeiro byte do parâmetro (P1) da unidade de dados do protocolo de aplicativo (APDU).
ms.assetid: 359df5cc-10a7-4093-9a77-f3eb0b98545a
title: 'ISCardCmd: método de ut_P1 de:p (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_P1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 18f7563fd6ae1c3490e36896b22af3a6034168e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749894"
---
# <a name="iscardcmdput_p1-method"></a>Método ISCardCmd::p UT \_ P1

\[O método de **Put \_ P1** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **Put \_ P1** define o primeiro byte do parâmetro (P1) da [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) (APDU).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_P1(
  [in] BYTE byP1
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*byP1* \[ no\]
</dt> <dd>

O byte que é o campo P1.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/>  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro *byP1* não é válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                     |



 

## <a name="remarks"></a>Comentários

Para definir o valor P2 do APDU, chame [**Get \_ P2**](iscardcmd-get-p2.md).

Para recuperar os valores P1, P2 e P3 existentes, chame [**Get \_ P1**](iscardcmd-get-p1.md), [**Get \_ P2**](iscardcmd-get-p2.md) ou [**Get \_ P3**](iscardcmd-get-p3.md) respectivamente.

Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como definir o primeiro byte do parâmetro (P1) da [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) (APDU). O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .


```C++
HRESULT  hr;

// Set the P1 byte.
hr = pISCardCmd->put_P1(0x06);
if (FAILED(hr))
{
  printf("Failed put_P1\n");
  // Take other error handling action as needed.
}
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

[**obter \_ P1**](iscardcmd-get-p1.md)
</dt> <dt>

[**obter \_ P2**](iscardcmd-get-p2.md)
</dt> <dt>

[**obter \_ P3**](iscardcmd-get-p3.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**colocar \_ P2**](iscardcmd-put-p2.md)
</dt> </dl>

 

 
