---
title: Propriedades padrão
description: Propriedades padrão
ms.assetid: 08b7c388-a362-4d71-ac24-93675984881f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78ab30dd644231c5c11a9f1e4d7ccf9c861ae2fa
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008401"
---
# <a name="standard-properties"></a>Propriedades padrão

O OLE define um conjunto de DISPIDs padrão para todos os três tipos de propriedades: controle, ambiente e estendido. As tabelas a seguir listam esses padrões para propriedades de controle, propriedades de ambiente e propriedades estendidas.



| Propriedade Controle                                                                               | Tipo                             | Descrição                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BackColor, ForeColor, FillColor, BorderColor<br/>                                        | **\_cor OLE**<br/>        | O esquema de cores do controle<br/>                                                                                                                                                                                                    |
| BackStyle, EstiloDePreenchimento, BorderStyle, BorderWidth, BorderVisible, DrawStyle, DrawWidth<br/> | **curto** ou **longo**<br/> | Bits que definem o comportamento visual de um controle, como Solid ou Transparent, tendo bordas espessas ou finas, estilos de linha e assim por diante.<br/>                                                                                    |
| Fonte<br/>                                                                                | **IDispatch \***<br/>      | A fonte usada no controle, que é um ponteiro **IDispatch** para um objeto de fonte padrão. Consulte [objeto de fonte padrão](standard-font-object.md) para obter mais informações.<br/>                                                         |
| Legenda, texto<br/>                                                                       | **BSTR**<br/>              | Cadeias de caracteres que contêm o rótulo do controle (a legenda) ou seu conteúdo textual (o texto). Observe que a legenda não necessariamente nomear o controle no contêiner. Consulte a propriedade nome estendido na tabela a seguir.<br/> |
| habilitado<br/>                                                                             | **BOOL**<br/>              | Determina se o controle está habilitado ou desabilitado. Se desabilitado, o controle provavelmente ficará acinzentado.<br/>                                                                                                                           |
| Janela<br/>                                                                              | **HWND**<br/>              | O identificador de janela do controle, se tiver um.<br/>                                                                                                                                                                              |
| TabStop<br/>                                                                             | **BOOL**<br/>              | Determina se este controle é uma parada de tabulação.<br/>                                                                                                                                                                                |



 



| Propriedade de ambiente                         | Tipo                        | Descrição                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BackColor, ForeColor<br/>          | **\_cor OLE**<br/>   | Fornece controles com as cores de plano de fundo padrão e de primeiro plano. O uso por um controle é opcional.<br/>                                                                                                                                                                                                                                                                                          |
| Fonte<br/>                          | **IDispatch \***<br/> | Um ponteiro para um objeto de fonte padrão que define a fonte padrão para o formulário. O uso por um controle é opcional. Consulte [objeto de fonte padrão](standard-font-object.md) para obter mais informações.<br/>                                                                                                                                                                                                    |
| LocaleID<br/>                      | **LCID**<br/>         | O idioma usado no contêiner. O uso de um controle é recomendado.<br/>                                                                                                                                                                                                                                                                                                                        |
| Modo<br/>                      | **BOOL**<br/>         | Descreve se o contêiner está em um modo de design (**false**) ou em modo de execução (**verdadeiro**), que um controle deve usar para alterar sua funcionalidade disponível conforme necessário.<br/>                                                                                                                                                                                                                      |
| UIDead<br/>                        | **BOOL**<br/>         | Descreve se o contêiner está em um modo em que os controles devem ignorar a entrada do usuário. Isso se aplica independentemente de UserMode. Um contêiner sempre pode definir UIDead como **true** no modo de design e pode defini-lo como **true** quando tiver atingido um ponto de interrupção ou tal durante o modo de execução. Um controle deve prestar atenção a essa propriedade.<br/>                                                                |
| MessageReflect<br/>                | **BOOL**<br/>         | Especifica se o contêiner deseja receber mensagens do Windows como o WM \_ CTLCOLOR, o WM \_ DRAWITEM, o WM \_ PARENTNOTIFY e assim por diante como eventos.<br/>                                                                                                                                                                                                                                           |
| SupportsMnemonics<br/>             | **BOOL**<br/>         | Descreve se o contêiner processa mnemônicos ou não. Um controle pode fazer tudo o que desejar com essas informações, como caracteres não sublinhados que normalmente usaria como um mnemônico.<br/>                                                                                                                                                                                                 |
| ShowGrabHandles, estou hachurando<br/> | **BOOL**<br/>         | Descreve se um controle deve mostrar uma borda de hachura ou alças de captura (na borda de hachura) quando ativo no local. Os controles devem obedecer a essas propriedades, dando ao contêiner controle final sobre quem realmente desenha esses bits da interface do usuário. Um contêiner de controle pode querer desenhar seu próprio em vez de depender de cada controle; nesse caso, esses ambientes serão sempre **falsos**.<br/> |
| DisplayAsDefault<br/>              | **BOOL**<br/>         | O contêiner vai expor um **verdadeiro** para essa propriedade por meio de qualquer site que contenha o que está marcado como o botão padrão quando o controle de botão deve se desenhar com um quadro padrão mais espesso.<br/>                                                                                                                                                                                         |



 



| Propriedade estendida          | Tipo                        | Descrição                                                           |
|----------------------------|-----------------------------|-----------------------------------------------------------------------|
| Nome<br/>            | **BSTR**<br/>         | O nome do contêiner para o controle.<br/>                      |
| Visible<br/>         | **BOOL**<br/>         | A visibilidade do controle.<br/>                                  |
| Pai<br/>          | **IDispatch \***<br/> | A dispinterface do formulário que contém o controle.<br/>      |
| Padrão, cancelar<br/> | **BOOL**<br/>         | Indica se esse controle é o padrão ou o botão Cancelar.<br/> |



 

Todas essas propriedades padrão têm valores DISPID negativos, indicando seu status padrão.

Observe que para evitar conflitos nos símbolos programáticos para esses DISPIDs, todas as propriedades de ambiente recebem símbolos na forma de propriedade de ambiente DISPID, \_ \_  como na cor de baixo do \_ ambiente DISPID \_ . Todos os outros símbolos usam \_ a *Propriedade* DISPID como de costume.

Algumas propriedades de ambiente, bem como propriedades de controle, envolvem cores. O tipo de **\_ cor OLE** mencionado nas tabelas anteriores pode se referir a um tipo **COLORREF** padrão, um índice para uma paleta, um índice relativo à paleta ou um índice de cores do sistema usado com a função [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) . A função [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor) converte um tipo de **\_ cor OLE** em um tipo **COLORREF** dado uma paleta.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades de controle](control-properties.md)
</dt> </dl>

 

