---
description: Inicia o Assistente do Passport quando usado com Rundll32.exe.
title: Função PassportWizardRunDll
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PassportWizardRunDll
api_type:
- DllExport
api_location:
- Netplwiz.dll
ms.assetid: 015c3875-698e-4d80-bbfc-4fc8a71197b7
ms.openlocfilehash: 7b75f4f3371814d00cf5b58dc12854763318c7ee424f35c7a7e6dad9f7734058
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820616"
---
# <a name="passportwizardrundll-function"></a>Função PassportWizardRunDll

\[Essa função está disponível por meio Windows XP com Service Pack 2 (SP2) e Windows Server 2003. Ele pode ser alterado ou não disponível nas versões subsequentes do Windows.\]

Inicia o Assistente do Passport quando usado com Rundll32.exe.

## <a name="syntax"></a>Sintaxe


```C++
void PassportWizardRunDll(
  _In_ HWND      hwndStub,
  _In_ HINSTANCE hAppInstance,
  _In_ LPTSTR    lpszCmdLine,
  _In_ int       nCmdShow
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwndStub* \[ Em\]
</dt> <dd>

Digite: **HWND**

Um alça para uma janela de proprietário. Normalmente, esse parâmetro é definido como **NULL.**

</dd> <dt>

*hAppInstance* \[ Em\]
</dt> <dd>

Tipo: **HINSTANCE**

Um handle para o arquivo de biblioteca, obtido como um valor de retorno de [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("netplwiz").

</dd> <dt>

*lpszCmdLine* \[ Em\]
</dt> <dd>

Tipo: **LPTSTR**

Dados de argumento. Esse valor sempre estará vazio.

</dd> <dt>

*nCmdShow* \[ Em\]
</dt> <dd>

Tipo: **int**

Define o modo de exibição para a janela.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Nenhum.

## <a name="remarks"></a>Comentários

O Assistente do Passport é usado para obter um Passport padrão para Windows. Um Passport fornece ao usuário acesso personalizado a todos os sites do MSN e outros sites habilitados para Passport usando o endereço de email do usuário. Usar **PassportWizardRunDll** como um ponto de entrada no arquivo Netplwiz.dll por meio de um comando Rundll32 permite que você iniciar o Assistente do Passport em uma linha de comando como se fosse um arquivo executável.

**PassportWizardRunDll** é usado exclusivamente no contexto de um Rundll32.exe da seguinte maneira:

**rundll32.exe netplwiz.dll, PassportWizardRunDll**

Usar uma função de ponto de entrada com Rundll32.exe não se parece com uma chamada de função normal. O nome da função e o nome do arquivo .dll no qual ele está armazenado são usados apenas como parâmetros de linha de comando. A definição de função mostrada em Sintaxe é apenas um protótipo padrão para todas as funções que você pode chamar usando Rundll32. Os valores específicos para *hwndStub,* *hAppInstance* e *nCmdShow* não são fornecidos pelo usuário, mas são tratados em segundo plano pelo Rundll32. **PassportWizardRunDll** não usa o valor *lpszCmdLine,* portanto, nenhum dado adicional é necessário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                            |
| Cabeçalho<br/>                   | <dl> <dt>Nenhum</dt> </dl>                                 |
| DLL<br/>                      | <dl> <dt>Netplwiz.dll (versão 5.60 ou posterior)</dt> </dl> |



 

 
