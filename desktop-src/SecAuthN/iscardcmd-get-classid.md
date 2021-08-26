---
description: Recupera o identificador de classe da APDU (unidade de dados do protocolo de aplicativo).
ms.assetid: 03ea997d-7698-43c7-aa9a-dfc1bac6fcdd
title: Método ISCardCmd::get_ClassId (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ee3f19c625924bd3620e3b19cc0fbd46857fda3079896ddbac1040f6718758f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015006"
---
# <a name="iscardcmdget_classid-method"></a>Método ClassId ISCardCmd::get \_

\[O **método \_ get ClassId** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O **método \_ get ClassId** recupera o identificador de classe da APDU (unidade de dados do protocolo [*de*](../secgloss/a-gly.md) aplicativo).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_ClassId(
  [out] BYTE *pbyClass
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbyClass* \[ out\]
</dt> <dd>

Ponteiro para o byte que representa o identificador de classe.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/>       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O *parâmetro pbyClass* não é válido.<br/>  |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | Um ponteiro ruim foi passado em *pbyClass.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                          |



 

## <a name="remarks"></a>Comentários

Para definir o identificador de classe como um novo valor, chame [**put \_ ClassId**](iscardcmd-put-classid.md).

Para ver uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).

Além dos códigos de erro COM listados acima, essa interface poderá retornar um código de erro de cartão inteligente se uma função de cartão inteligente tiver sido chamada para concluir a solicitação. Para obter mais informações, consulte [Valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como recuperar a ID da classe. O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd.**](iscardcmd.md)


```C++
BYTE     byClassID;
HRESULT  hr;

// Retrieve the class ID.
hr = pISCardCmd->get_ClassId(&byClassID);
if (FAILED(hr))
{
  printf("Failed get_ClassId\n");
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

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**put \_ ClassId**](iscardcmd-put-classid.md)
</dt> </dl>

 

 
