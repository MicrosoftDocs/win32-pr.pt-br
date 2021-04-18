---
title: Propriedades predefinidas (msctf. h)
description: Os valores a seguir identificam as propriedades definidas pelo TSF. O formato de dados e o conteúdo de cada tipo de propriedade são incluídos.
ms.assetid: d88f2eba-4c98-4b32-96e1-cd019fe0f7ad
keywords:
- Propriedades predefinidas estrutura de serviços de texto
topic_type:
- apiref
api_name:
- Predefined Properties
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 807d1be5d1cc025971ad294fac825b89a4a0a519
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810471"
---
# <a name="predefined-properties"></a>Propriedades predefinidas

Os valores a seguir identificam as propriedades definidas pelo TSF. O formato de dados e o conteúdo de cada tipo de propriedade são incluídos.

## <a name="properties"></a>Propriedades



| Propriedade                        | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_atributo prop de GUID \_**       | Contém um valor [**TfGuidAtom**](tfguidatom.md) que representa o **GUID** do atributo de exibição. [**ITfCategoryMgr:: GetGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid) é usado para converter esse valor em um **GUID**. Para obter mais informações, consulte [usando atributos de exibição](using-display-attributes.md).                                                                                                                                                                                                                                                                                                                                                                             |
| **xmlowner prop do GUID \_ \_**       | Contém um valor [**TfGuidAtom**](tfguidatom.md) que representa o identificador de classe ( **CLSID** ) do serviço de texto que possui o texto. [**ITfCategoryMgr:: GetGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid) é usado para converter esse valor em um **CLSID**.                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **LangID de GUID de \_ prop \_**          | Contém um valor **DWORD** que contém o identificador de idioma ( **LangID** ) do texto na palavra inferior.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **\_leitura da prop GUID \_**         | Contém o texto de leitura fonético do texto coberto pela propriedade. Isso pode ser diferente do texto real. Os aplicativos da Windows Store não dão suporte a essa propriedade.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **\_composição da props GUID \_**       | Contém um valor booliano que é diferente de zero se o texto faz parte de uma composição ou zero caso contrário. Se essa propriedade for VT \_ vazia, pode ser pressuposto que o texto não faz parte de uma composição.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **\_MODEBIAS prop de GUID \_**        | Contém um valor [**TfGuidAtom**](tfguidatom.md) que representa o tipo de tendência de modo com suporte. [**ITfCategoryMgr:: GetGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid) é usado para converter esse valor em um **GUID**. Pode ser um dos valores de [**tendência de modo**](mode-bias-values.md).                                                                                                                                                                                                                                                                                                                                                                                                  |
| **PROP de GUID \_ \_ adora meu lifeATTICE**       | Contém um ponteiro para um objeto [**ITfLMLattice**](/windows/desktop/api/Ctffunc/nn-ctffunc-itflmlattice) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **\_ \_ TKB \_ alternações de prop de GUID** | **A partir do Windows 8:** Contém um valor **DWORD** definido pelo teclado de toque. Essa propriedade pode ser usada por controles de edição com reconhecimento de TSF e aplicativos para identificar a natureza do texto no intervalo de texto coberto pela propriedade, por exemplo, se o texto no intervalo resultar da inserção de uma sugestão de texto ou correção automática. <br/> A natureza do texto no intervalo de texto coberto pela propriedade também se estende ao tipo de alternativas que seriam retornadas pela interface [**ITfFnReconversion**](/windows/desktop/api/Ctffunc/nn-ctffunc-itffnreconversion) para esse intervalo de texto no documento.<br/> Consulte os comentários a seguir para obter os possíveis valores dessa propriedade.<br/> |



 

## <a name="remarks"></a>Comentários

A **propriedade \_ \_ TKB \_ Alternate do GUID prop** pode ser um dos valores a seguir.



| Nome                                     | Valor      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_padrão de alternativas \_ TKB                | 0x00000001 | Indica que o teclado de toque gerou uma lista de possíveis palavras alternativas para o texto no intervalo coberto pela propriedade, e que nem o intervalo de texto nem as alternativas são uma sugestão de correção automática ou de texto.                                                                                                                                                                                                              |
| TKB \_ alternativas \_ para \_ correção automática     | 0x00000002 | Indica que o teclado de toque gerou uma palavra alternativa que deve substituir automaticamente o texto no intervalo de texto coberto pela propriedade.<br/> O teclado de toque não aplicará a correção automática sem ser instruído a fazer isso pelo controle ou aplicativo de edição. A interface de reconversão ([**ITfFnReconversion**](/windows/desktop/api/Ctffunc/nn-ctffunc-itffnreconversion)) deve ser usada para aplicar a correção ao texto no documento.<br/> |
| TKB \_ alternativas \_ para \_ previsão         | 0x00000003 | Indica que o intervalo de texto coberto pela propriedade é uma sugestão de texto que foi gerada pelo teclado de toque e inserida no documento pelo usuário.<br/> Previsões alternativas adicionais também podem ser armazenadas como uma propriedade no documento.<br/>                                                                                                                                                                     |
| \_correção automática de alternativas de TKB \_ \_ aplicada | 0x00000004 | Indica que o intervalo de texto coberto pela propriedade é uma correção automática fornecida pelo teclado de toque e aplicada por meio da interface [**ITfFnReconversion**](/windows/desktop/api/Ctffunc/nn-ctffunc-itffnreconversion) .<br/> Esse valor pode ser usado por controles de edição ou aplicativos, com \_ alternativas TKB \_ para \_ correção automática, para evitar a aplicação repetida de uma correção automática.<br/>                                                                               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                      |
| parâmetro<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TfGuidAtom**](tfguidatom.md)
</dt> <dt>

[**ITfCategoryMgr:: GetGuid**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[Usando atributos de exibição](using-display-attributes.md)
</dt> <dt>

[**Valores de tendência do modo**](mode-bias-values.md)
</dt> <dt>

[**ITfLMLattice**](/windows/desktop/api/Ctffunc/nn-ctffunc-itflmlattice)
</dt> </dl>

 

 





