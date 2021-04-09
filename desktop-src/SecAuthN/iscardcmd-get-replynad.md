---
description: Recupera o endereço do nó (NAD) usado pelo cartão inteligente na mensagem de resposta.
ms.assetid: bf4f281c-d378-4abd-8f2e-e23c2f4e87a4
title: 'Método ISCardCmd:: get_ReplyNad (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyNad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2088aa208a97511fd53eecec5a8cdc473b612bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090464"
---
# <a name="iscardcmdget_replynad-method"></a>Método ISCardCmd:: get \_ ReplyNad

\[O método **Get \_ ReplyNad** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **Get \_ ReplyNad** recupera o endereço de nó (NAD) usado pelo [*cartão inteligente*](../secgloss/s-gly.md) na mensagem de resposta.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_ReplyNad(
  [out] BYTE *pbNad
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbNad* \[ fora\]
</dt> <dd>

Ponteiro para o byte que contém o NAD usado pela mensagem de resposta, no retorno.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                    | Descrição                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | A operação foi concluída com êxito.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | O parâmetro *pbNad* não é válido.<br/>                     |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Chamadas internas não puderam recuperar informações da NAD.<br/> |



 

## <a name="remarks"></a>Comentários

Além dos códigos de erro COM listados acima, esse método pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como recuperar o endereço do nó (NAD) usado pelo [*cartão inteligente*](../secgloss/s-gly.md) na mensagem de resposta. O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .


```C++
BYTE    byNad;
HRESULT hr;

// Get reply Nad.
hr = pISCardCmd->get_ReplyNad(&byNad);
if (FAILED(hr))
{
  printf("Failed get_ReplyNad\n");
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

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
