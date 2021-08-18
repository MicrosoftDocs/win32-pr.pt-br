---
description: Recupera a APDU (unidade de dados de protocolo de aplicativo bruto).
ms.assetid: d8b326db-de54-4ef8-becb-fd905414c45c
title: Método ISCardCmd::get_Apdu (Scarddat.h)
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
ms.openlocfilehash: 773185563db798877d38d3fb877fe1b4459468e4eeb4d45aed922203bd813418
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015086"
---
# <a name="iscardcmdget_apdu-method"></a>Método ISCardCmd::get \_ Apdu

\[O **método \_ get Apdu** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O **método \_ get Apdu** recupera a APDU (unidade de dados do protocolo [*de*](../secgloss/a-gly.md) aplicativo bruto).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Apdu(
  [out] LPBYTEBUFFER *ppApdu
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppApdu* \[ out\]
</dt> <dd>

Ponteiro para o buffer de byte mapeado por meio de **um objeto IStream** que contém a mensagem APDU no retorno.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O *parâmetro ppApdu* não é válido.<br/>  |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | Um ponteiro ruim foi passado em *ppApdu.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                        |



 

## <a name="remarks"></a>Comentários

Para copiar o APDU de um objeto [**IByteBuffer**](ibytebuffer.md) (**IStream**) para o APDU envolvido nesse objeto de interface, chame [**put \_ Apdu**](iscardcmd-put-apdu.md).

Para determinar o comprimento do APDU, chame [**get \_ ApduLength.**](iscardcmd-get-apdulength.md)

Para ver uma lista de todos os métodos fornecidos pela interface [**ISCardCmd,**](iscardcmd.md) [**consulte ISCardCmd**](iscardcmd.md).

Além dos códigos de erro COM listados acima, essa interface poderá retornar um código de erro de cartão inteligente se uma função de cartão inteligente tiver sido chamada para concluir [*a*](../secgloss/s-gly.md) solicitação. Para obter informações sobre códigos de erro de cartão inteligente, consulte [Valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como recuperar a APDU (unidade de dados do protocolo [*de*](../secgloss/a-gly.md) aplicativo bruto). O exemplo supõe que pISCardCmd é um ponteiro válido para a interface [**ISCardCmd**](iscardcmd.md) e que pIByteApdu é um ponteiro válido para uma instância da interface [**IByteBuffer.**](ibytebuffer.md)


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

[**get \_ ApduLength**](iscardcmd-get-apdulength.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**put \_ Apdu**](iscardcmd-put-apdu.md)
</dt> </dl>

 

 
