---
description: Recupera o terceiro byte do parâmetro (P3) da unidade de dados do protocolo de aplicativo (APDU).
ms.assetid: 5fe90686-f542-42be-91ed-6600eaee3e7b
title: 'Método ISCardCmd:: get_P3 (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_P3
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b1072fc9c4ca3b2a238cc8893104df1a831c99c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090466"
---
# <a name="iscardcmdget_p3-method"></a>Método ISCardCmd:: get \_ P3

\[O método **Get \_ P3** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **Get \_ P3** recupera o terceiro byte do parâmetro (P3) da [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) (APDU). Esse valor de byte somente leitura representa o tamanho da parte de dados do APDU.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_P3(
  [out] BYTE *pbyP3
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbyP3* \[ fora\]
</dt> <dd>

Ponteiro para o byte que é P3 do APDU no retorno.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/>    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O *pbyP3* não é válido.<br/>            |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um ponteiro inadequado foi passado em *pbyP3*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                       |



 

## <a name="remarks"></a>Comentários

O parâmetro P3 é somente leitura e, portanto, não pode ser definido.

Para obter os parâmetros P1 ou P2, chame [**Get \_ P1**](iscardcmd-get-p1.md) e [**Get \_ P2**](iscardcmd-get-p2.md) , respectivamente.

Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como recuperar o terceiro byte do parâmetro (P3) da [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) (APDU). O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .


```C++
BYTE  byP3;
HRESULT  hr;

// Retrieve the P3 byte.
hr = pISCardCmd->get_P3(&byP3);
if (FAILED(hr))
{
  printf("Failed get_P3\n");
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

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
