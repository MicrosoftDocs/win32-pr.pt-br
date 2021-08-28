---
description: A função AddPrintProvidor instala um provedor de impressão local e vincula a configuração, os dados e os arquivos do provedor.
ms.assetid: f34549c3-0474-48ba-9307-5b36f02dbe1c
title: Função AddPrintProvidor (winspool. h)
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
ms.openlocfilehash: c5738f2a9dbf7da4a2dcddb952891b415af73cb7
ms.sourcegitcommit: 58ca2495eae63806264bf4594db45aae692c70b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "122021690"
---
# <a name="addprintprovidor-function"></a>Função AddPrintProvidor

> [!IMPORTANT]
> Em 6 de julho de 2021, o [KB5005010](https://support.microsoft.com/topic/kb5005010-restricting-installation-of-new-printer-drivers-after-applying-the-july-6-2021-updates-31b91c02-05bc-4ada-a7ea-183b129578a7) introduziu uma opção de configuração baseada no registro opcional para restringir o acesso a essa API apenas aos usuários administradores. Essa opção estava desativada como padrão.
>
> Em 10 de agosto de 2021, [KB5005652](https://aka.ms/print_install_kb) altera o valor padrão dessa configuração para exigir direitos de administrador para instalar novos drivers de impressora.

A função **AddPrintProvidor** instala um provedor de impressão local e vincula a configuração, os dados e os arquivos do provedor.

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

*pname* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor no qual o provedor deve ser instalado. Para sistemas que dão suporte apenas à instalação local de provedores, esse parâmetro deve ser **nulo**.

</dd> <dt>

*Nível* \[ do no\]
</dt> <dd>

O nível da estrutura à qual *pProviderInfo* aponta. Pode ser um dos seguintes.



| Valor                                                                                                | Significado                                                                            |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | A função usa uma estrutura [**PROVIDOR \_ info \_ 1**](providor-info-1.md) .<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | A função usa uma estrutura [**PROVIDOR \_ info \_ 2**](providor-info-2.md) .<br/> |



 

</dd> <dt>

*pProviderInfo* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de provedor de impressão, conforme indicado pelo *nível*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

Antes que um aplicativo chame a função **AddPrintProvidor** , todos os arquivos exigidos pelo provedor devem ser copiados para o diretório system32.

Um provedor adicionado pelo **AddPrintProvidor** pode ser removido chamando [**DeletePrintProvidor**](deleteprintprovidor.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **AddPrintProvidorW** (Unicode) e **AddPrintProvidorA** (ANSI)<br/>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrintProvidor**](deleteprintprovidor.md)
</dt> <dt>

[**Informações de PROVIDOR \_ \_ 1**](providor-info-1.md)
</dt> <dt>

[**Informações de PROVIDOR \_ \_ 2**](providor-info-2.md)
</dt> </dl>

 

 




