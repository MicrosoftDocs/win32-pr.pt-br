---
description: Recupera a APDU (unidade de dados do protocolo de aplicativo bruto).
ms.assetid: d8b326db-de54-4ef8-becb-fd905414c45c
title: 'Método ISCardCmd:: get_Apdu (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_Apdu
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: fb943d7ade48f6684cdc10cb4b1ad7e48f87e65c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010510"
---
# <a name="iscardcmdget_apdu-method"></a>Método ISCardCmd:: get \_ APDU

\[O método **Get \_ APDU** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **Get \_ APDU** recupera a APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) bruto).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Apdu(
  [out] LPBYTEBUFFER *ppApdu
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppApdu* \[ fora\]
</dt> <dd>

Ponteiro para o buffer de bytes mapeado por meio de um objeto **IStream** que contém a mensagem APDU no retorno.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro *ppApdu* não é válido.<br/>  |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um ponteiro inadequado foi passado em *ppApdu*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                        |



 

## <a name="remarks"></a>Comentários

Para copiar o APDU de um objeto [**IByteBuffer**](ibytebuffer.md) (**IStream**) para o APDU encapsulado neste objeto de interface, chame [**Put \_ APDU**](iscardcmd-put-apdu.md).

Para determinar o comprimento do APDU, chame [**Get \_ ApduLength**](iscardcmd-get-apdulength.md).

Para obter uma lista de todos os métodos fornecidos pela interface [**ISCardCmd**](iscardcmd.md) , consulte [**ISCardCmd**](iscardcmd.md).

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter informações sobre códigos de erro de cartão inteligente, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como recuperar a APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) bruto). O exemplo supõe que pISCardCmd é um ponteiro válido para a interface [**ISCardCmd**](iscardcmd.md) e que pIByteApdu é um ponteiro válido para uma instância da interface [**IByteBuffer**](ibytebuffer.md) .


```C++
HRESULT    hr;

hr = pISCardCmd->get_Apdu(&pIByteApdu);
if (FAILED(hr)) 
{
    printf("Failed get_Apdu.\n");
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

[**obter \_ ApduLength**](iscardcmd-get-apdulength.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**colocar \_ APDU**](iscardcmd-put-apdu.md)
</dt> </dl>

 

 
