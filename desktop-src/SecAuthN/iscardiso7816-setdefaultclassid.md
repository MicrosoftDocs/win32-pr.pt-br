---
description: O método SetDefaultClassId atribui um byte de identificador de classe padrão que será usado em todas as operações ao construir uma APDU (unidade de dados do protocolo de aplicativo de comando) ISO 7816-4. Por padrão, o byte do identificador de classe padrão é 0x00.
ms.assetid: 5a53d5f1-7986-4c4c-9512-f592cd398d1c
title: 'Método ISCardISO7816:: SetDefaultClassId (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.SetDefaultClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d242d83af00bb0d8e10d7da22d014a31deafaa66f49fb509cc91b65263239dd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481103"
---
# <a name="iscardiso7816setdefaultclassid-method"></a>Método ISCardISO7816:: SetDefaultClassId

\[O método **SetDefaultClassId** está disponível para uso nos sistemas operacionais especificados na seção requisitos. ele não está disponível para uso no Windows server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **SetDefaultClassId** atribui um byte de identificador de classe padrão que será usado em todas as operações ao construir uma APDU (unidade de [*dados do protocolo de aplicativo*](../secgloss/a-gly.md) de comando) ISO 7816-4. Por padrão, o byte do identificador de classe padrão é 0x00.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetDefaultClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*byClass* \[ no\]
</dt> <dd>

Byte de ID de classe.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Os possíveis valores de retorno são os seguintes:



| Código de retorno                                                                          | Descrição                                  |
|--------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Operação concluída com sucesso.<br/> |



 

Para obter uma lista de todos os métodos fornecidos pela interface [**ISCardISO7816**](iscardiso7816.md) , consulte **ISCardISO7816**.

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter informações sobre códigos de erro de cartão inteligente, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardsrv. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 é definido como 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
