---
description: Contém ponteiros para funções de retorno de chamada que podem ser usadas pelas funções do CSP (provedor de serviços de criptografia).
ms.assetid: 84a379e9-c6b9-4c1d-bbbb-9bed4a045d90
title: Estrutura VTableProvStruc (Cspdk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VTableProvStruc
- VTableProvStrucW
api_type:
- HeaderDef
api_location:
- Cspdk.h
ms.openlocfilehash: 99b9344c6951dc93972315d9b4f60752f1484d68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663141"
---
# <a name="vtableprovstruc-structure"></a>Estrutura VTableProvStruc

A estrutura **VTableProvStruc** contém ponteiros para funções de retorno de chamada que podem ser usadas pelas funções do CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct VTableProvStruc {
  DWORD   Version;
  FARPROC FuncVerifyImage;
  FARPROC FuncReturnhWnd;
  DWORD   dwProvType;
  BYTE    *pbContextInfo;
  DWORD   cbContextInfo;
  LPSTR   pszProvName;
} VTableProvStruc, *PVTableProvStruc;
```



## <a name="members"></a>Membros

<dl> <dt>

**Versão**
</dt> <dd>

Um valor **DWORD** que indica a versão da estrutura. Três versões desta estrutura são usadas. As versões são número 1, 2 e 3 e determinam quais membros da estrutura são válidos. Os membros da versão 1 são válidos em todos os sistemas que dão suporte a essa estrutura.

Este é um membro da versão 1.

</dd> <dt>

**FuncVerifyImage**
</dt> <dd>

O endereço de uma função de retorno de chamada [**FuncVerifyImage**](funcverifyimage.md) que o CSP usa para verificar a assinatura de quaisquer DLLs que o CSP carregará. Todas as DLLs auxiliares nas quais um CSP faz chamadas de função devem ser assinadas da mesma maneira (e com a mesma chave) que a DLL do CSP primário. Para garantir essa assinatura, as DLLs auxiliares devem ser carregadas dinamicamente usando a função [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) . Mas, antes que a DLL seja carregada, a assinatura da DLL deve ser verificada. O CSP executa essa verificação chamando a função **FuncVerifyImage** , conforme mostrado no exemplo abaixo.

Esse ponteiro de função pode ser armazenado e usado até que o contexto do CSP seja liberado.

Este é um membro da versão 1.

</dd> <dt>

**FuncReturnhWnd**
</dt> <dd>

O endereço de uma função de retorno de chamada [**FuncReturnhWnd**](funcreturnhwnd.md) que retorna o identificador de janela que o CSP deve usar como pai ou proprietário de qualquer interface do usuário que é exibida. Os CSPs que não se comunicam diretamente com o usuário e os CSPs que usam hardware dedicado para essa finalidade podem ignorar essa entrada. Esse identificador de janela é zero por padrão, mas um aplicativo pode definir isso com um valor diferente usando a função [**CryptSetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam) para definir a propriedade de **\_ \_ HWND de cliente PP** .

Esse ponteiro de função pode ser armazenado e usado até que o contexto do CSP seja liberado.

Este é um membro da versão 1.

</dd> <dt>

**dwProvType**
</dt> <dd>

Um valor **DWORD** que especifica o tipo de provedor a ser adquirido. Os seguintes [*tipos de provedor*](../secgloss/p-gly.md) são predefinidos e são discutidos em detalhes na [interoperabilidade do CSP](https://www.bing.com/search?q=CSP+Interoperability):

-   PROV \_ RSA \_ completo
-   PROV \_ RSA \_ SIG
-   PROV \_ DSS
-   PROV \_ Fortezza
-   PROV \_ MS \_ Exchange

Este é um membro da versão 2.

</dd> <dt>

**pbContextInfo**
</dt> <dd>

Um ponteiro para uma matriz de informações de contexto. Os membros **pbContextInfo** e **cbContextInfo** juntos determinam o conjunto de informações usado quando uma função [**CPSETPROVPARAM**](https://www.bing.com/search?q=**CPSetProvParam**) é chamada com o PP do conjunto de \_ informações de contexto \_ .

Este é um membro da versão 2.

</dd> <dt>

**cbContextInfo**
</dt> <dd>

Um valor **DWORD** que indica o número de elementos na matriz **pbContextInfo** .

Este é um membro da versão 2.

</dd> <dt>

**pszProvName**
</dt> <dd>

Uma cadeia de caracteres que contém o nome do provedor.

Este é um membro da versão 3.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os ponteiros na estrutura **VTableProvStruc** só estão disponíveis na função [**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**) . Se os membros da estrutura forem necessários depois que uma chamada para **CPAcquireContext** for concluída, as cópias dos elementos de estrutura necessários deverão ser feitas pelo CSP. Os ponteiros de função nessa estrutura podem ser armazenados e usados até que o contexto do CSP seja liberado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Cspdk. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **VTableProvStrucW** (Unicode)<br/>                                          |



 

 
