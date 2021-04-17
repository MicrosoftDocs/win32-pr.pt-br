---
description: O método encapsulate encapsula a APDU (unidade de dados do protocolo de aplicativo) de comando fornecida em outro APDU de comando para transmissão para um cartão inteligente.
ms.assetid: dfffad09-046b-46cb-b6fd-286a4bbf1066
title: 'Método ISCardCmd:: encapsulate (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.Encapsulate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: cd671a11edd9977695eeaf858e38f962b3dd0962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748552"
---
# <a name="iscardcmdencapsulate-method"></a>Método ISCardCmd:: encapsulate

\[O método **encapsulate** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **encapsulate** encapsula a APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ) de comando fornecida em outro APDU de comando para transmissão para um [*cartão inteligente*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Encapsulate(
  [in] LPBYTEBUFFER  pApdu,
  [in] ISO_APDU_TYPE ApduType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pApdu* \[ no\]
</dt> <dd>

Ponteiro para o APDU a ser encapsulado.

</dd> <dt>

*ApduType* \[ no\]
</dt> <dd>

Caso ISO 7816-4 para transmissões [*T = 0*](../secgloss/t-gly.md) .

<dl><span id="ISO_CASE_1"></span><span id="iso_case_1"></span><dt>

**\_Caso ISO \_ 1**
</dt><span id="ISO_CASE_2"></span><span id="iso_case_2"></span><dt>

**\_Caso ISO \_ 2**
</dt><span id="ISO_CASE_3"></span><span id="iso_case_3"></span><dt>

**\_Caso ISO \_ 3**
</dt><span id="ISO_CASE_4"></span><span id="iso_case_4"></span><dt>

**\_Caso ISO \_ 4**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/>    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parâmetro inválido.<br/>                   |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um ponteiro inadequado foi passado em *pApdu*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                       |



 

## <a name="remarks"></a>Comentários

Para criar um comando APDU, chame [**BuildCmd**](iscardcmd-buildcmd.md).

Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como encapsular um comando APDU. O exemplo supõe que pIByteApdu é um ponteiro válido para uma instância da interface [**IByteBuffer**](ibytebuffer.md) .


```C++
HRESULT    hr;

// pIByteApdu is a pointer to an instance of IByteBuffer.
// Encapsulate the APDU.
hr = pISCardCmd->Encapsulate(pIByteApdu, ISO_CASE_1);
if (FAILED(hr)) 
{
    printf("Failed Encapsulate.\n");
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

[**BuildCmd**](iscardcmd-buildcmd.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
