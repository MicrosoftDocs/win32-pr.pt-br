---
description: Define um novo identificador de classe na APDU (unidade de dados do protocolo de aplicativo).
ms.assetid: 7e7d42f2-2858-4b37-a7d5-a919e3e005da
title: Método ISCardCmd::p ut_ClassId (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: c632b25e3fcef3f08b79dffa6f72dcc7ae3409d744de02527b3be495638b2ba9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014596"
---
# <a name="iscardcmdput_classid-method"></a>Método ClassId ISCardCmd::p ut \_

\[O **método \_ put ClassId** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O **método \_ put ClassId** define um novo identificador de classe na APDU (unidade de dados [*do*](../secgloss/a-gly.md) protocolo de aplicativo).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_ClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*byClass* \[ Em\]
</dt> <dd>

O byte que representa o identificador de classe.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O *byClass* não é válido.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                    |



 

## <a name="remarks"></a>Comentários

Para recuperar o identificador de classe atual, chame [**get \_ ClassId.**](iscardcmd-get-classid.md)

Para ver uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).

Além dos códigos de erro COM listados acima, essa interface poderá retornar um código de erro de cartão inteligente se uma função de cartão inteligente tiver sido chamada para concluir [*a*](../secgloss/s-gly.md) solicitação. Para obter mais informações, consulte [Valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como definir um novo identificador de classe na APDU (unidade de dados do protocolo [*de*](../secgloss/a-gly.md) aplicativo). O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd.**](iscardcmd.md)


```C++
HRESULT  hr;

// Set the class ID.
hr = pISCardCmd->put_ClassId(0xC0);
if (FAILED(hr))
{
  printf("Failed put_ClassId\n");
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

[**get \_ ClassId**](iscardcmd-get-classid.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
