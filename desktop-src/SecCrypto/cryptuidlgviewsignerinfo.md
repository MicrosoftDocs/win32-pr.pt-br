---
description: Exibe uma caixa de diálogo que contém as informações de signatário de uma mensagem assinada.
ms.assetid: e4552cbb-90f4-46f4-a271-3a91ccd5f806
title: Função CryptUIDlgViewSignerInfo
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: 7ae677692b9266893eabf1002039c5efbf0ca5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826985"
---
# <a name="cryptuidlgviewsignerinfo-function"></a>Função CryptUIDlgViewSignerInfo

\[A função **CryptUIDlgViewSignerInfo** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. \]

A função **CryptUIDlgViewSignerInfo** exibe uma caixa de diálogo que contém as informações de signatário de uma mensagem assinada.

> [!Note]  
> Essa função não é declarada em um arquivo de cabeçalho publicado. Para usar essa estrutura, declare-a no formato exato mostrado.

## <a name="syntax"></a>Sintaxe


```C++
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pcvsi* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ \_ struct CRYPTUI VIEWSIGNERINFO**](cryptui-viewsignerinfo-struct.md) que contém as informações de signatário a serem exibidas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função retorna um valor diferente de zero em caso de êxito e zero em caso de falha. Para obter informações de erro estendidas, chame a função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

Os códigos de erro possíveis retornados de [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) incluem, mas não se limitam a, o seguinte.



| Código de retorno                                                                                   | Descrição                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Um ou mais argumentos não são válidos.<br/>  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Ocorreu uma falha de alocação de memória.<br/> |

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                        |
| Fim do suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                       |
| Biblioteca<br/>                  | <dl> <dt>Cryptui. lib</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>Cryptui.dll</dt> </dl>      |
| Nomes Unicode e ANSI<br/>   | **CryptUIDlgViewSignerInfoW** (Unicode) e **CryptUIDlgViewSignerInfoA** (ANSI)<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CRYPTUI \_ VIEWSIGNERINFO \_ struct**](cryptui-viewsignerinfo-struct.md)
</dt> </dl>
