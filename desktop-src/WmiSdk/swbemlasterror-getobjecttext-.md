---
description: O método GetObjectText do objeto SWbemLastError retorna uma renderização textual do objeto em um formato \_ Managed Object Format (MOF).
ms.assetid: efe3f3f6-c2f2-4295-bbf3-60d5b06ef98f
ms.tgt_platform: multiple
title: SWbemLastError.GetObjectText_ método (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7f935457c6fa6566d69c10b6cb5cade914e6e81c175f7451cc6eaff5268358e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679586"
---
# <a name="swbemlasterrorgetobjecttext_-method"></a>Método SWbemLastError.GetObjectText \_

O **método GetObjectText \_** do objeto [**SWbemLastError**](swbemlasterror.md) retorna uma renderização textual do objeto em um formato [Managed Object Format (MOF).](managed-object-format--mof-.md) Esse objeto MOF pode ser usado para exibir o conteúdo de um objeto. Observe que o texto MOF retornado não contém todas as informações sobre o objeto, mas apenas informações suficientes para que o compilador MOF possa criar o objeto original. Por exemplo, você não encontrará nenhuma informação sobre os qualificadores propagados ou as propriedades da classe pai.

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
strMofText = .GetObjectText_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iFlags* \[ in, opcional\]
</dt> <dd>

Esse parâmetro é reservado e deve ser 0 (zero) se especificado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se for bem-sucedido, esse método retornará uma cadeia de caracteres que contém o texto de saída.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do **método \_ GetObjectText,** o **objeto Err** pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Um parâmetro especificado não é válido.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLastError<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemLastError<br/>                                                         |



 

 




