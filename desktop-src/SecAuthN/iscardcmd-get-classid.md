---
description: Recupera o identificador de classe da APDU (unidade de dados do protocolo de aplicativo).
ms.assetid: 03ea997d-7698-43c7-aa9a-dfc1bac6fcdd
title: 'Método ISCardCmd:: get_ClassId (Scarddat. h)'
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
ms.openlocfilehash: 6b78dfc9f3adf200a614b129ff1e86a16c88438f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090469"
---
# <a name="iscardcmdget_classid-method"></a>Método ISCardCmd:: get \_ ClassID

\[O método **Get \_ ClassID** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **Get \_ ClassID** recupera o identificador de classe da APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_ClassId(
  [out] BYTE *pbyClass
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbyClass* \[ fora\]
</dt> <dd>

Ponteiro para o byte que representa o identificador de classe.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/>       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro *pbyClass* não é válido.<br/>  |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um ponteiro inadequado foi passado em *pbyClass*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                          |



 

## <a name="remarks"></a>Comentários

Para definir o identificador de classe como um novo valor, chame [**Put \_ ClassID**](iscardcmd-put-classid.md).

Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como recuperar a ID de classe. O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .


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
</dt> <dt>

[**colocar \_ ClassID**](iscardcmd-put-classid.md)
</dt> </dl>

 

 
