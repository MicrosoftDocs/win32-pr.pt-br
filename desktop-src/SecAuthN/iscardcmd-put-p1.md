---
description: Define o primeiro byte de parâmetro (P1) da APDU (unidade de dados do protocolo de aplicativo).
ms.assetid: 359df5cc-10a7-4093-9a77-f3eb0b98545a
title: Método ISCardCmd::p ut_P1 (Scarddat.h)
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
ms.openlocfilehash: 7375a04928cf58dc9ef73b6463f2c7d2b19144649e21d7b3220f981584f4c63b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008135"
---
# <a name="iscardcmdput_p1-method"></a>Método ISCardCmd::p ut \_ P1

\[O **método \_ put P1** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O **método \_ put P1** define o primeiro byte de parâmetro (P1) da APDU (unidade de dados [*do*](../secgloss/a-gly.md) protocolo de aplicativo).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_P1(
  [in] BYTE byP1
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*byP1* \[ Em\]
</dt> <dd>

O byte que é o campo P1.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/>  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O *parâmetro byP1* não é válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                     |



 

## <a name="remarks"></a>Comentários

Para definir o valor P2 do APDU, chame [**get \_ P2**](iscardcmd-get-p2.md).

Para recuperar os valores P1, P2 e P3 existentes, chame [**get \_ P1**](iscardcmd-get-p1.md), [**get \_ P2**](iscardcmd-get-p2.md) ou [**get \_ P3,**](iscardcmd-get-p3.md) respectivamente.

Para ver uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).

Além dos códigos de erro COM listados acima, essa interface poderá retornar um código de erro de cartão inteligente se uma função de cartão inteligente tiver sido chamada para concluir [*a*](../secgloss/s-gly.md) solicitação. Para obter mais informações, consulte [Valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como definir o primeiro byte de parâmetro (P1) da APDU (unidade de dados [*do*](../secgloss/a-gly.md) protocolo de aplicativo). O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd.**](iscardcmd.md)


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
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCardCmd é definido como \_ D5778AE3-43DE-11D0-9171-00AAA00C18068<br/>            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**get \_ P1**](iscardcmd-get-p1.md)
</dt> <dt>

[**get \_ P2**](iscardcmd-get-p2.md)
</dt> <dt>

[**get \_ P3**](iscardcmd-get-p3.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**put \_ P2**](iscardcmd-put-p2.md)
</dt> </dl>

 

 
