---
description: Recupera o valor da ID de classe alternativa.
ms.assetid: 80c7cbba-e28d-4973-9f3f-7636ff331b64
title: 'Método ISCardCmd:: get_AlternateClassId (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_AlternateClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8cfc47011881ae3e3f6df5ef51c910899a054f84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748466"
---
# <a name="iscardcmdget_alternateclassid-method"></a>Método ISCardCmd:: get \_ AlternateClassId

\[O método **Get \_ AlternateClassId** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **Get \_ AlternateClassId** recupera o valor da ID de classe alternativa. Esse método falhará a menos que a ID alternativa tenha sido definida por uma chamada anterior para [**Put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_AlternateClassId(
  [out] BYTE *pbyClass
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbyClass* \[ fora\]
</dt> <dd>

Ponteiro para o byte que contém o valor de ID de classe alternativo no retorno.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna os seguintes valores possíveis.



| Código de retorno                                                                                    | Descrição                                                                                                                                 |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | A operação foi concluída com êxito.<br/>                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | O parâmetro *pbyClass* não é válido.<br/>                                                                                           |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | A ID de classe alternativa não foi definida anteriormente por uma chamada para [**Put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).<br/> |



 

## <a name="remarks"></a>Comentários

Esse método se aplica a comunicações usando o [*protocolo T = 0*](../secgloss/t-gly.md). Para obter mais informações, consulte [**Put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como recuperar a ID de classe alternativa. O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .


```C++
BYTE     byAltClassID;
HRESULT  hr;

// Retrieve the alternate class ID.
hr = pISCardCmd->get_AlternateClassId(&byAltClassID);
if (FAILED(hr))
{
  printf("Failed get_AltClassId\n");
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

[**colocar \_ AlternateClassId**](iscardcmd-put-alternateclassid.md)
</dt> </dl>

 

 
