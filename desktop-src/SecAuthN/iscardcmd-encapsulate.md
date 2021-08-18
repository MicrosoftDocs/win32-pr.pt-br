---
description: O método Encapsular encapsula a APDU (unidade de dados do protocolo de aplicativo de comando) em outro comando APDU para transmissão para um cartão inteligente.
ms.assetid: dfffad09-046b-46cb-b6fd-286a4bbf1066
title: Método ISCardCmd::Encapsulate (Scarddat.h)
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
ms.openlocfilehash: f531d0d5f55bea1fe63875a9feb508eb8b4c0e830705bfad2603cc52664c6f44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015116"
---
# <a name="iscardcmdencapsulate-method"></a>Método ISCardCmd::Encapsulate

\[O **método Encapsular** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O **método Encapsular** encapsula a APDU [*(unidade*](../secgloss/a-gly.md) de dados do protocolo de aplicativo de comando) em outro comando APDU para transmissão para um [*cartão inteligente*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Encapsulate(
  [in] LPBYTEBUFFER  pApdu,
  [in] ISO_APDU_TYPE ApduType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pApdu* \[ Em\]
</dt> <dd>

Ponteiro para o APDU a ser encapsulado.

</dd> <dt>

*ApduType* \[ Em\]
</dt> <dd>

Caso ISO 7816-4 para [*transmissões T=0.*](../secgloss/t-gly.md)

<dl><span id="ISO_CASE_1"></span><span id="iso_case_1"></span><dt>

**CASO ISO \_ \_ 1**
</dt><span id="ISO_CASE_2"></span><span id="iso_case_2"></span><dt>

**CASO ISO \_ \_ 2**
</dt><span id="ISO_CASE_3"></span><span id="iso_case_3"></span><dt>

**CASO ISO \_ \_ 3**
</dt><span id="ISO_CASE_4"></span><span id="iso_case_4"></span><dt>

**CASO ISO \_ \_ 4**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/>    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parâmetro inválido.<br/>                   |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | Um ponteiro ruim foi passado em *pApdu.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                       |



 

## <a name="remarks"></a>Comentários

Para criar um comando APDU, chame [**BuildCmd**](iscardcmd-buildcmd.md).

Para ver uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).

Além dos códigos de erro COM listados acima, essa interface poderá retornar um código de erro de cartão inteligente se uma função de cartão inteligente tiver sido chamada para concluir a solicitação. Para obter mais informações, consulte [Valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como encapsular um comando APDU. O exemplo pressupor que pIByteApdu é um ponteiro válido para uma instância da interface [**IByteBuffer.**](ibytebuffer.md)


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

[**BuildCmd**](iscardcmd-buildcmd.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
