---
description: Contém informações para a função CryptUIDlgViewSignerInfo.
ms.assetid: 2b76de4f-4b35-477e-a67e-435434e066c6
title: Estrutura de CRYPTUI_VIEWSIGNERINFO_STRUCT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPTUI_VIEWSIGNERINFO_STRUCT
- CRYPTUI_VIEWSIGNERINFO_STRUCTA
- CRYPTUI_VIEWSIGNERINFO_STRUCTW
api_type:
- NA
api_location: ''
ms.openlocfilehash: da150da6b5115e20a78a4edca64a5c9a97f66132
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104011012"
---
# <a name="cryptui_viewsignerinfo_struct-structure"></a>\_Estrutura de \_ struct CRYPTUI VIEWSIGNERINFO

\[A estrutura de **\_ \_ struct CRYPTUI VIEWSIGNERINFO** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]

A estrutura de **\_ \_ struct CRYPTUI VIEWSIGNERINFO** contém informações para a função [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) .

> [!Note]  
> Essa estrutura não é declarada em um arquivo de cabeçalho publicado. Para usar essa estrutura, declare-a no formato exato mostrado.

 

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagCRYPTUI_VIEWSIGNERINFO_STRUCT {
  DWORD            dwSize;
  HWND             hwndParent;
  DWORD            dwFlags;
  LPCTSTR          szTitle;
  CMSG_SIGNER_INFO *pSignerInfo;
  HCRYPTMSG        hMsg;
  LPCSTR           pszOID;
  DWORD_PTR        dwReserved;
  DWORD            cStores;
  HCERTSTORE       *rghStores;
  DWORD            cPropSheetPages;
  LPCPROPSHEETPAGE rgPropSheetPages;
} CRYPTUI_VIEWSIGNERINFO_STRUCT, *PCRYPTUI_VIEWSIGNERINFO_STRUCT;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwSize**
</dt> <dd>

O tamanho, em bytes, dessa estrutura.

</dd> <dt>

**hwndParent**
</dt> <dd>

O identificador da janela para ser o pai da caixa de diálogo. Esse membro pode ser **nulo** se a caixa de diálogo não deve ter nenhum pai.

</dd> <dt>

**dwFlags**
</dt> <dd>

Um conjunto de sinalizadores que modifica o comportamento da função [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) . Não há sinalizadores definidos no momento, portanto, esse membro deve ser zero.

</dd> <dt>

**szTitle**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o título a ser exibido na caixa de diálogo. Se esse membro for **nulo**, será usado um título padrão.

</dd> <dt>

**pSignerInfo**
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ \_ informações de signatário CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_info) que contém as informações de signatário a serem exibidas.

</dd> <dt>

**hMsg**
</dt> <dd>

O identificador da mensagem da qual as informações de signatário foram extraídas.

</dd> <dt>

**pszOID**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres ANSI terminada em nulo que contém a representação de cadeia de caracteres do [*identificador de objeto*](../secgloss/o-gly.md) (OID) que significa para qual o certificado que fez a assinatura deve ser validado. Por exemplo, se isso estiver sendo chamado para exibir a assinatura de uma CTL ( [*lista de certificados confiáveis*](../secgloss/c-gly.md) ), a cadeia de caracteres do OID de **assinatura de uso do szOID \_ KP \_ CTL \_ \_** deverá ser passada. Se esse membro for **nulo**, o certificado não será validado para usos.

</dd> <dt>

**dwReserved**
</dt> <dd>

Este parâmetro não é usado no momento. Este membro deve ser **nulo**.

</dd> <dt>

**cStores**
</dt> <dd>

O número de elementos na matriz **rghStores** .

</dd> <dt>

**rghStores**
</dt> <dd>

Uma matriz de valores **HCERTSTORE** que representam os outros repositórios de certificados para pesquisar o certificado que assinou a mensagem. Se esse membro for **nulo**, nenhum repositório adicional será pesquisado. O membro **cStores** contém o número de elementos nesta matriz.

</dd> <dt>

**cPropSheetPages**
</dt> <dd>

O número de elementos na matriz **rgPropSheetPages** .

</dd> <dt>

**rgPropSheetPages**
</dt> <dd>

Uma matriz de ponteiros de estrutura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) que definem páginas adicionais a serem exibidas na caixa de diálogo padrão. Se esse membro for **nulo**, nenhuma página adicional será exibida. O membro **cPropSheetPages** contém o número de elementos nesta matriz.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                      |
| Nomes Unicode e ANSI<br/>   | **CRYPTUI \_ VIEWSIGNERINFO \_ STRUCTW** (Unicode) e **CRYPTUI \_ VIEWSIGNERINFO \_ structA** (ANSI)<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md)
</dt> </dl>

 

 
