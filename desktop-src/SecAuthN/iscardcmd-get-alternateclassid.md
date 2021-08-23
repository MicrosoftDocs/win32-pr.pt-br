---
description: Recupera o valor da ID de classe alternativa.
ms.assetid: 80c7cbba-e28d-4973-9f3f-7636ff331b64
title: Método ISCardCmd::get_AlternateClassId (Scarddat.h)
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
ms.openlocfilehash: ac6d74f89eaf2c42ec9fc00cef9d82735b4b28885180c3c5d429dad7450e3c74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577776"
---
# <a name="iscardcmdget_alternateclassid-method"></a>Método ISCardCmd::get \_ AlternateClassId

\[O **método \_ get AlternateClassId** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O **método \_ get AlternateClassId** recupera o valor da ID de classe alternativa. Esse método falhará, a menos que a ID alternativa tenha sido definida por uma chamada anterior para [**colocar \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_AlternateClassId(
  [out] BYTE *pbyClass
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbyClass* \[ out\]
</dt> <dd>

Ponteiro para o byte que contém o valor da ID de classe alternativa no retorno.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna os seguintes valores possíveis.



| Código de retorno                                                                                    | Descrição                                                                                                                                 |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | A operação foi concluída com êxito.<br/>                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | O *parâmetro pbyClass* não é válido.<br/>                                                                                           |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | A ID de classe alternativa não foi definida anteriormente por uma chamada para [**colocar \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).<br/> |



 

## <a name="remarks"></a>Comentários

Esse método se aplica às comunicações usando o [*protocolo T=0*](../secgloss/t-gly.md). Para obter mais informações, [**consulte put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como recuperar a ID de classe alternativa. O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd.**](iscardcmd.md)


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

[**put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md)
</dt> </dl>

 

 
