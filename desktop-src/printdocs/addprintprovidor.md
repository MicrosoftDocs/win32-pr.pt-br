---
description: A função AddPrintProvidor instala um provedor de impressão local e vincula a configuração, os dados e os arquivos do provedor.
ms.assetid: f34549c3-0474-48ba-9307-5b36f02dbe1c
title: Função AddPrintProvidor (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrintProvidor
- AddPrintProvidorA
- AddPrintProvidorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: ca968397441765455e74059201c128be53f50916e5e28212c700078f52124fe8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868731"
---
# <a name="addprintprovidor-function"></a>Função AddPrintProvidor

A **função AddPrintProvidor** instala um provedor de impressão local e vincula a configuração, os dados e os arquivos do provedor.

## <a name="syntax"></a>Sintaxe


```C++
BOOL AddPrintProvidor(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pProviderInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pName* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor no qual o provedor deve ser instalado. Para sistemas que só suportam a instalação local de provedores, esse parâmetro deve ser **NULL.**

</dd> <dt>

*Nível* \[ Em\]
</dt> <dd>

O nível da estrutura para a qual *pProviderInfo* aponta. Pode ser um dos seguintes.



| Valor                                                                                                | Significado                                                                            |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | A função usa uma [**estrutura PROVIDOR \_ INFO \_ 1.**](providor-info-1.md)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | A função usa uma [**estrutura PROVIDOR \_ INFO \_ 2.**](providor-info-2.md)<br/> |



 

</dd> <dt>

*pProviderInfo* \[ Em\]
</dt> <dd>

Um ponteiro para uma estrutura do provedor de impressão, conforme indicado por *Level*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um valor não zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração do servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

Antes que um aplicativo chama **a função AddPrintProvidor,** todos os arquivos exigidos pelo provedor devem ser copiados para o diretório SYSTEM32.

Um provedor adicionado por **AddPrintProvidor** pode ser removido chamando [**DeletePrintProvidor.**](deleteprintprovidor.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **AddPrintProvidorW** (Unicode) e **AddPrintProvidorA** (ANSI)<br/>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrintProvidor**](deleteprintprovidor.md)
</dt> <dt>

[**INFORMAÇÕES DO \_ PROVIDOR \_ 1**](providor-info-1.md)
</dt> <dt>

[**INFORMAÇÕES DO \_ PROVIDOR \_ 2**](providor-info-2.md)
</dt> </dl>

 

 




